<template>
	<div class="layout">
		<Layout>
			<Header>
				<Menu mode="horizontal" theme="dark" active-name="1">
					<div class="layout-logo"></div>
					<div class="layout-nav">
						<MenuItem name="1">
						<Icon type="ios-navigate"></Icon>
						Item 1
						</MenuItem>
						<MenuItem name="2">
						<Icon type="ios-keypad"></Icon>
						Item 2
						</MenuItem>
						<MenuItem name="3">
						<Icon type="ios-analytics"></Icon>
						Item 3
						</MenuItem>
						<MenuItem name="4">
						<Icon type="ios-paper"></Icon>
						<!-- Item 4 -->
						<router-link to="/">Home</router-link>
						</MenuItem>
					</div>
				</Menu>
			</Header>
			<Layout>
				<Sider hide-trigger :style="{background: '#fff'}">
					<Menu active-name="1-2" theme="light" width="auto" :open-names="['1']">
						<Submenu name="1">
							<template slot="title">
								<Icon type="ios-navigate"></Icon>
								Item 1
							</template>
							<!-- 使用 router-link 组件来导航. -->
							<!-- 通过传入 `to` 属性指定链接. -->
							<!-- <router-link> 默认会被渲染成一个 `<a>` 标签 -->
							<MenuItem name="1-1">
								<router-link to="/可乐">Home</router-link>
							</MenuItem>
							<MenuItem name="1-2">
								<router-link to="/about/12312">About</router-link>
							</MenuItem>
							<MenuItem name="1-3">Option 3</MenuItem>
						</Submenu>
						<Submenu name="2">
							<template slot="title">
								<Icon type="ios-keypad"></Icon>
								Item 2
							</template>
							<MenuItem name="2-1">Option 1</MenuItem>
							<MenuItem name="2-2">Option 2</MenuItem>
						</Submenu>
						<Submenu name="3">
							<template slot="title">
								<Icon type="ios-analytics"></Icon>
								Item 3
							</template>
							<MenuItem name="3-1">Option 1</MenuItem>
							<MenuItem name="3-2">Option 2</MenuItem>
						</Submenu>
					</Menu>
				</Sider>
				<Layout :style="{padding: '0 24px 24px'}">
					<Breadcrumb :style="{margin: '24px 0'}">
						<BreadcrumbItem>Home</BreadcrumbItem>
						<BreadcrumbItem>Components</BreadcrumbItem>
						<BreadcrumbItem>Layout</BreadcrumbItem>
					</Breadcrumb>
					<Content :style="{padding: '24px', minHeight: '280px', background: '#fff'}">
						<!-- 路由出口 -->
						<!-- 路由匹配到的组件将渲染在这里 -->
						<div style="border: 1px solid red; height: 400px;">
						<router-view></router-view>
						</div>
					</Content>
				</Layout>
			</Layout>
		</Layout>
	</div>
</template>
<script>
	//导入组件
	import Home from '@/views/Home'
	import About from '@/views/About'
	export default {
		components: { //注册组件
			Home,
			About
		}
	}
</script>
<style scoped>
	.layout {
		border: 1px solid #d7dde4;
		background: #f5f7f9;
		position: relative;
		border-radius: 4px;
		overflow: hidden;
	}

	.layout-logo {
		width: 100px;
		height: 30px;
		background: #5b6270;
		border-radius: 3px;
		float: left;
		position: relative;
		top: 15px;
		left: 20px;
	}

	.layout-nav {
		width: 420px;
		margin: 0 auto;
		margin-right: 20px;
	}
</style>
