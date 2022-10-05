<template>
	<view>
		<view class="login" v-show="isAuthorization">
			<view class="uni-common-mt">
				<view class="uni-form-item uni-column">
					<view class="login_label">
						登录
					</view>
					<view class="uni-form-item uni-column">
						<view>
							<input class="uni-input" v-model="username" focus placeholder="账号"/>
						</view>
					</view>
					<view class="uni-form-item uni-column">
						<view>
							<input class="uni-input" v-model="password" hold-keyboard placeholder="密码" password="true">
						</view>
					</view>
					<view class="uni-form-item uni-column">
						<view>
							<button type="primary" @click="user_login">登录</button>
						</view>
					</view>
				</view>
			</view>
		</view>
		<view class="message" v-show="!isAuthorization">
			A Page
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				isAuthorization: true
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss" scoped>
	.login {
		padding: 20rpx 40rpx;
		margin: 200rpx 20rpx;
		text-align: center;
		background-color: #eee;

		.login_label {
			color: #333333;
			margin: 0 auto;
		}

		.uni-input {
			background-color: #fff;
			height: 80rpx;
			text-align: left;
			padding-left: 10rpx;
			border-radius: 10rpx;
			font-size: 30rpx;
		}

		.uni-form-item {
			margin: 30rpx 0;
		}

		button {
			font-size: 30rpx;
		}
	}

	.message {
		.message_item {
			display: flex;
			padding: 15rpx 20rpx;
			border-bottom: 1px solid #eee;

			image {
				border-radius: 10rpx;
				width: 100rpx;
				min-width: 100rpx;
				max-width: 100rpx;
				height: 80rpx;
			}

			.right {
				margin-left: 15rpx;

				.message_content {
					font-size: 27rpx;
					color: #555555;
					margin-bottom: 10rpx;
				}

				.message_channel {
					display: flex;
					font-size: 25rpx;
					color: #999999;

					.info {
						float: left;
						margin-left: 30rpx;
						font-size: 25rpx;
						color: #999999;

					}

				}
			}
		}
	}
</style>

