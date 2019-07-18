<template>
<div>
	<el-row v-for="(a, i) in 2" :key="a">
		<el-col v-for="(o, index) in 4" :key="o" :offset='index%4'>
			<el-card>
				<el-image :src="cards[i*4 + index].path"></el-image>
				<span class='card__name'>{{cards[i*4 + index].name}}</span>
			</el-card>
		</el-col>
	</el-row>
	<el-carousel>
		<el-carousel-item v-for="item in carousels" :key="item">
			<img :src="item">
		</el-carousel-item>
	</el-carousel>
</div>
</template>


<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import vueImage from '../../assets/logo.png';

@Component({})

export default class PrimaryPage extends Vue{
		
	private data() {
		return {
			cards :[{
				name: '儿童保险',
				path: vueImage
			}, {
				name: '成人保险',
				path: vueImage
			}, {
				name: '老人保险',
				path: vueImage
			}, {
				name: '女性专区',
				path: vueImage
			},{
				name: '方案设计',
				path: vueImage
			}, {
				name: '大V解读',
				path: vueImage
			}, {
				name: '其他保险',
				path: vueImage
			}, {
				name: '理财专区',
				path: vueImage
			}],
			carousels : []
		}
	}
}
</script>>


<style>
	.el-row {
		display: flex;
		flex-direction: row;
	}

	.el-col {
		flex-grow: 1;
	}

	.card__name {
		display: block;
	}
</style>
