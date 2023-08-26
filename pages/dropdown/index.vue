<template>
	<view class="dropdown-demo">
		<button @click="toggleDropdown" class="fa fa-angle-down" style="font-size: 29px;"></button>
		<view v-show="isDropdownOpen" class="dropdown-menu">
			<!-- 下拉菜单的内容 -->
			<text @click="selectOption('Option 1')">
				<navigator url="/pages/index/index">test</navigator>
			</text>
			<text @click="selectOption('Option 2')">选项 2</text>
			<text @click="selectOption('Option 3')">选项 3</text>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				isDropdownOpen: false,
				selectedOption: ''
			};
		},
		methods: {
			toggleDropdown() {
				this.isDropdownOpen = !this.isDropdownOpen;
			},
			selectOption(option) {
				this.selectedOption = option;
				this.isDropdownOpen = false;
			}
		}
	};
</script>

<style>
	.dropdown-demo {
		position: relative;
		width: 100%;
		height: 100vh;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.dropdown-menu {
		position: absolute;
		top: 40px;
		right: 0;
		width: 120px;
		background-color: #fff;
		border: 1px solid #ccc;
		box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
		z-index: 1;
	}

	.dropdown-menu {
		display: flex;
		padding: 8px;
		cursor: pointer;
		flex-direction: column;
	}
</style>