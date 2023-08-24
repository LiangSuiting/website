<template>
	<view style="width: 100%;height: 70px;background-color: rgb(19, 14, 14);" class="flex">
		<view style="flex:1;height: 70px;background-color: rgb(0, 0, 0);">
			<navigator url="/pages/index/index">
				<image src="/static/logo1.png" width="60%" height="70px" style="margin-left:10% ;width: 60%;height: 70px;"></image>
			</navigator>
		</view>
		<view style="flex:4;height: 70px;"></view>
		<view style="flex:1;height: 70px;background-color: rgb(53, 53, 53);" class="flex">
			<view style="height: 70px;width: 70px;">
				<image src="/static/touxiang.png" style="border-radius: 50%;width: 70px;height: 70px;"></image>
			</view>
			<view style="flex:1;height: 70px;background-color: blue;" class="flex">
				<view style="flex:7;background-color: rgb(71, 69, 69);height: 70px;" class="column">
					<view style="margin: auto;text-align: center;overflow: auto;color: white;">Xeanen</view>
				</view>
			</view>
		</view>
	</view>
	<view class="flex">
		<view style="background-color:rgb(51,51 ,51);height: 100vh;" class="flex1">
			<navigator url="/pages/announcement/index" style="color: white;text-decoration: none">
				<view style="width: 100%;background-color: rgb(37,38 ,38);height: 7%;margin-top: 5px;">
					<button type="button"
						style="width: 100%;height: 100%;border-radius: 15px;cursor: pointer;background-color: rgb(30,30,30);border: 0px;color: white;font-size: large;"
						class="yyan">
						公告
					</button>
				</view>
			</navigator>
			<navigator url="/pages/kaoqinjilu/index.html" style="color: white;text-decoration: none">
				<view style="width: 100%;background-color: rgb(37,38 ,38);height: 7%;margin-top: 5px;">
					<button type="button"
						style="width: 100%;height: 100%;border-radius: 15px;cursor: pointer;background-color: rgb(30,30,30);border: 0px;color: white;font-size: large;"
						class="yyan">
						考勤记录
					</button>
				</view>
			</navigator>
			<navigator url="/pages/qingjia/index.html" style="color: white;text-decoration: none">
				<view style="width: 100%;background-color: rgb(37,38 ,38);height: 7%;margin-top: 5px;">
					<button type="button"
						style="width: 100%;height: 100%;border-radius: 15px;cursor: pointer;background-color: rgb(30,30,30);border: 0px;color: white;font-size: large;"
						class="yyan">
						请假
					</button>
				</view>
			</navigator>
		</view>
		<view class="flex6"
			style="height:100vh;overflow:auto;background-color:rgb(30,30,30);display: flex;align-items:center;">
			<view style="margin: auto;">
				<view class="date">
					{{time}}
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				time: ""
			}
		},
		onLoad() {
			document.title = "总览";
			this.timer = setInterval(() => this.changeTime(), 50)
		},
		onUnload() {
			clearInterval(this.timer)
		},
		methods: {
			changeTime() {
				this.time = new Date().toLocaleString()
			}
		}
	}
</script>

<style>
	.flex {
		display: flex;
	}

	.flex1 {
		flex: 1
	}

	.flex6 {
		flex: 6
	}

	.column {
		display: flex;
		flex-direction: column;
	}

	.flex2 {
		flex: 2;
	}

	.yyan:hover {
		box-shadow: 0px 0px 5px 5px rgb(183, 48, 38);
	}

	body {
		margin: 0px;
	}

	.dingwei {
		position: fixed;
		top: 40px;
		left: -65px;
	}

	.dropdown {
		position: relative;
	}

	.dropdown-content {
		display: none;
		position: absolute;
		background-color: #525252;
		width: 90px;
		height: 300px;
		margin-top: 0px;
	}

	.dropdown:focus .dropdown-content {
		display: block;
		right: 0;
	}

	.date {
		width: 70rem;
		height: 100px;
		text-align: center;
		vertical-align: middle;
		line-height: 100px;
		font-size: 80px;
		color: white;
	}
</style>