<template>
	<view style="width: 100%;height: 70px;background-color: rgb(19, 14, 14);" class="flex">
		<view style="flex:1;height: 70px;background-color: rgb(0, 0, 0);" @click="ganbixialacaidan">
			<image src="/static/logo1.png" style="margin-left:10% ;width: 60%;height: 70px;"></image>
		</view>
		<view style="flex:4;height: 70px;" @click="ganbixialacaidan"></view>
		<view style="flex:1;height: 70px;background-color: rgb(53, 53, 53);" class="flex">
			<view style="height: 70px;width: 70px;" @click="ganbixialacaidan">
				<image src="/static/touxiang.png" style="border-radius: 50%;width: 70px;height: 70px;"></image>
			</view>
			<view style="flex:1;height: 70px;background-color: blue;" class="flex">
				<view style="width: 80%;background-color: rgb(71, 69, 69);height: 70px;" class="column"
					@click="ganbixialacaidan">
					<view style="margin: auto;text-align: center;overflow: auto;color: white;">Xeanen</view>
				</view>
				<view style="height: 70px;background-color: rgb(133, 130, 130);flex:1" class="column">
					<view class="xialatubiao">
						<view class="dropdown-demo">
							<button @click="toggleDropdown" style="background-color: rgb(133, 130, 130);">
								<text class="fa fa-angle-down" style="font-size: 29px;"></text>
							</button>
							<view v-show="isDropdownOpen" class="dropdown-menu">
								<!-- 下拉菜单的内容 -->
								<text @click="selectOption('Option 1')">
									<navigator url="/pages/index/index">test</navigator>
								</text>
								<text @click="selectOption('Option 2')">选项 2</text>
								<text @click="selectOption('Option 3')">选项 3</text>
							</view>
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
	<view class="flex" @click="ganbixialacaidan">
		<view style="background-color:rgb(51,51 ,51);height: 100vh;" class="flex1">
			<navigator url="/pages/index/index" style="color: white;text-decoration: none">
				<view style="width: 100%;background-color: rgb(37,38 ,38);height: 7%;margin-top: 5px;">
					<button type="button"
						style="width: 100%;height: 100%;border-radius: 15px;cursor: pointer;background-color: rgb(30,30,30);border: 0px;color: white;font-size: large;"
						class="yyan">
						首页
					</button>
				</view>
			</navigator>
		</view>
		<view class="flex6" style="height:100vh;background-color:rgb(30,30,30);overflow: hidden;">
			<image src="/static/welcome.jpg" style="width: 100%;height: 200px;"></image>
			<view style="width: 100%;height: 100px;margin-top: 80px;padding-left: 100px;font-size: 50px;color: white;">
				工作室</view>
			<view style="width: 100%;height: 150px;">
				<navigator url="/pages/zonglan/index" style="width: 250px;height: 150px;margin-left: 150px;">
					<view class="yyan kuang">
						总裁办公室
						<view style="color: gray;font-size: small;">中国夕宁有限公司广州总公司</view>
					</view>
				</navigator>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				isDropdownOpen: false,
				selectedOption: ''
			}
		},
		onLoad() {
			document.title = "首页"
		},
		methods: {
			toggleDropdown() {
				this.isDropdownOpen = !this.isDropdownOpen;
			},
			selectOption(option) {
				this.selectedOption = option;
				this.isDropdownOpen = false;
			},
			ganbixialacaidan() {
				this.isDropdownOpen = !this, isDropdownOpen;
			}
		}
	}
</script>

<style>
	@import "/font/css/font-awesome.css";
	@import "style.css";
</style>