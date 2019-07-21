<template>
	<div class = 'rollup'>
		<div class = 'rollupitem' v-for="(item, index) in items" :key="index">{{item.name}}</div>
	</div>
</template>

<script lang='ts' >
import { Component, Prop, Vue } from 'vue-property-decorator';
import anime from 'animejs';

interface RollupItemInfo {
	name :string;
	url :string;
}


/**
 * 向上滚动组件。
 */
@Component
export class Rollup extends Vue{

	private items: RollupItemInfo[];

	public mounted() {
		
	}
}
</script>

<style>
	.rollup {
		height: 30px;
	}

	.rollupitem {
		line-height: 30px;
	}
</style>
 