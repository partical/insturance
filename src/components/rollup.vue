<template>
	<div class = 'rollup'>
		<div class = 'rollupitem' v-for="(item, index) in rollupItems" :key="index">{{item.name}}</div>
	</div>
</template>

<script lang='ts' >
import { Component, Prop, Vue } from 'vue-property-decorator';
import anime from 'animejs/lib/anime.es.js';

interface RollupItemInfo {
	name :string;
	url :string;
}

/**
 * 向上滚动组件。
 */
@Component
export default class Rollup extends Vue{

	@Prop() private rollupItems!: RollupItemInfo[];

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
 