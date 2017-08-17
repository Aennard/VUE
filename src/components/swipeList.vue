<template>
	<div class="list">
		<swiper :options="swiperOption" >
			<swiper-slide v-for="item in imgArr">
				<img class="photo" :src="item.src"/>
			</swiper-slide>
			<div class="swiper-pagination" slot="pagination"></div>
		</swiper>
	</div>	
</template>

<script>
	import { swiper, swiperSlide } from 'vue-awesome-swiper'
	const imgArr = [{
		src:'/static/img/share_img.png'
	},{
		src:'/static/img/event_img.png'
	},{
		src:'/static/img/family_img.png'
	},{
		src:'/static/img/active_img.jpg'
	}];
	export default {
		name: 'swipeList',
		components: {
		swiper,
		swiperSlide
		},
		data() {
			return {
				swiperOption: {
					slidesPerView: 4,
					spaceBetween: 10,
				},
				imgArr: imgArr
			}
		}
  }
</script>

<style lang='scss'>
	.list {
		width:100%;
		display:block;
  	margin-bottom: -10px;
		
		.photo {
			height: 210px;
			}
	}

</style>
