<template>
<div>
	<el-row v-for="a in 2" :key="a">
		<el-col v-for="(o, index) in 4" :key="o">
			<el-card>
				<img :src="cards[index].path">
				<span>{{cards[index].name}}</span>
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
@Component({})

export default class PrimaryPage extends Vue{
		
	private data() {
		return {
			cards :[{
				name: '',
				path: ''
			}],
			carousels : []
		}
	}
}
</script>>
