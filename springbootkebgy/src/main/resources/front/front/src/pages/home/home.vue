<template>
<div class="home-preview" :style='{"width":"100%","margin":"0px auto","flexWrap":"wrap","justifyContent":"center","display":"flex"}'>


	<!-- 关于我们 -->
	<div :style='{"padding":"30px 7% 50px","boxShadow":"0 0px 0px rgba(255, 255, 255, .3)","margin":"0px auto 0px","flexWrap":"wrap","background":"#333","display":"flex","width":"100%","position":"relative","justifyContent":"flex-end","height":"auto"}'>
	  <div :style='{"margin":"60px 0 0 40px","color":"#e0be8d","textAlign":"center","left":"7%","background":"#333","width":"214px","lineHeight":"50px","fontSize":"32px","position":"absolute","height":"60px","zIndex":"11"}'>{{aboutUsDetail.title}}</div>
	  <div :style='{"margin":"0 0 0px","color":"#e0be8d","top":"138px","textAlign":"center","left":"7%","background":"#333","width":"214px","fontSize":"26px","position":"absolute","zIndex":"11"}'>{{aboutUsDetail.subtitle}}</div>
	  <div :style='{"width":"800px","padding":"0 10px","flexWrap":"wrap","display":"none","height":"100%"}'>
	    <img :style='{"margin":"0 10px","objectFit":"cover","flex":1,"display":"block","height":"120px"}' :src="baseUrl + aboutUsDetail.picture1">
	    <img :style='{"margin":"0 10px","objectFit":"cover","flex":1,"display":"block","height":"120px"}' :src="baseUrl + aboutUsDetail.picture2">
	    <img :style='{"margin":"0 10px","objectFit":"cover","flex":1,"display":"block","height":"120px"}' :src="baseUrl + aboutUsDetail.picture3">
	  </div>
	  <div :style='{"padding":"20px","margin":"0 0 0 0px","overflow":"hidden","color":"#e0be8d","background":"none","width":"calc(100% - 320px)","lineHeight":"24px","fontSize":"15px","textIndent":"2em","float":"right","height":"236px"}' v-html="aboutUsDetail.content"></div>
	  <div :style='{"top":"30px","left":"7%","background":"url(http://codegen.caihongy.cn/20230109/9922ef97a7c64c849de98056e07e7194.png) no-repeat center center","display":"block","width":"214px","position":"absolute","height":"232px"}' />
	  <div :style='{"width":"214px","background":"url(\"http://codegen.caihongy.cn/20201114/7856ba26477849ea828f481fa2773a95.jpg\") 0% 0% / cover no-repeat","display":"none","height":"232px"}' />
	  <div :style='{"width":"285px","background":"url(\"http://codegen.caihongy.cn/20201114/7856ba26477849ea828f481fa2773a95.jpg\") 0% 0% / cover no-repeat","display":"none","height":"100px"}' />
	  <div :style='{"width":"285px","background":"url(\"http://codegen.caihongy.cn/20201114/7856ba26477849ea828f481fa2773a95.jpg\") 0% 0% / cover no-repeat","display":"none","height":"100px"}' />
	</div>

<div class="recommend" :style='{"padding":"0 0 0px","margin":"0px auto","flexWrap":"wrap","background":"url() no-repeat center top,#faf0e6","display":"flex","width":"100%","position":"relative"}'>
	
    <div class="title" :style='{"padding":"0px 7%","margin":"40px auto 20px","alignItems":"flex-start","textAlign":"center","background":"none","flexDirection":"column","display":"flex","width":"100%","lineHeight":"54px","position":"relative","justifyContent":"flex-start","height":"32px"}'>
		<span :style='{"margin":"0 4px 0 0","fontSize":"20px","lineHeight":"24px","color":"#202020","fontWeight":"bold"}'>商城商品推荐</span>
	</div>
	
	<div v-if="true" class="idea recommendIdea" :style='{"width":"100%","padding":"0px 7%","flexWrap":"wrap","background":"#faf0e6","justifyContent":"space-between","display":"flex"}'>
		<div class="box1" :style='{"width":"100%","background":"url(http://codegen.caihongy.cn/20230110/bb7105350fc24c34a1b2d5d05e889ef6.jpg) no-repeat center center / 100% 100%","height":"280px"}'></div>
		<div class="box2" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box3" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box4" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box5" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box6" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box7" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box8" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box9" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box10" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
	</div>
	
	
	
	
	<!-- 样式四 -->
	<div class="list list4 index-pv1" :style='{"width":"100%","padding":"20px 7% 40px","background":"none","height":"auto"}'>
		<div v-if="shangchengshangpinRecommend.length>0" class="list-item animation-box" @click="toDetail('shangchengshangpinDetail', shangchengshangpinRecommend[0])" :style='{"width":"48%","margin":"0 0px","position":"relative","float":"left","height":"570px"}'>
			<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-if="preHttp(shangchengshangpinRecommend[0].shangpintupian)" :src="shangchengshangpinRecommend[0].shangpintupian.split(',')[0]" alt="" />
			<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-else :src="baseUrl + (shangchengshangpinRecommend[0].shangpintupian?shangchengshangpinRecommend[0].shangpintupian.split(',')[0]:'')" alt="" />
			<div class="title line1" :style='{"color":"#fff","left":"0","textAlign":"center","bottom":"0","background":"rgba(0,0,0,.3)","width":"100%","lineHeight":"44px","fontSize":"18px","position":"absolute"}'>
                <div>{{shangchengshangpinRecommend[0].shangpinmingcheng}}</div>
                <div>{{shangchengshangpinRecommend[0].shangpinzhonglei}}</div>
                <div>{{shangchengshangpinRecommend[0].dianpuming}}</div>
            </div>
		</div>
		<div class="list-body" :style='{"width":"48%","margin":"0 0 20px","float":"right","justifyContent":"space-between","display":"flex","height":"275px"}'>
			<div v-if="shangchengshangpinRecommend.length>1" @click="toDetail('shangchengshangpinDetail', shangchengshangpinRecommend[1])" class="list-item animation-box" :style='{"width":"48%","margin":"0 0px","position":"relative","display":"inline-block","height":"100%"}'>
				<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-if="preHttp(shangchengshangpinRecommend[1].shangpintupian)" :src="shangchengshangpinRecommend[1].shangpintupian.split(',')[0]" alt="" />
				<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-else :src="baseUrl + (shangchengshangpinRecommend[1].shangpintupian?shangchengshangpinRecommend[1].shangpintupian.split(',')[0]:'')" alt="" />
				<div class="title line1" :style='{"color":"#fff","left":"0","textAlign":"center","bottom":"0","background":"rgba(0,0,0,.3)","width":"100%","lineHeight":"44px","fontSize":"18px","position":"absolute"}'>
                    <div>{{shangchengshangpinRecommend[1].shangpinmingcheng}}</div>
                    <div>{{shangchengshangpinRecommend[1].shangpinzhonglei}}</div>
                    <div>{{shangchengshangpinRecommend[1].dianpuming}}</div>
                </div>
			</div>
			<div v-if="shangchengshangpinRecommend.length>2" @click="toDetail('shangchengshangpinDetail', shangchengshangpinRecommend[2])" class="list-item animation-box" :style='{"width":"48%","margin":"0 0px","position":"relative","display":"inline-block","height":"100%"}'>
				<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-if="preHttp(shangchengshangpinRecommend[2].shangpintupian)" :src="shangchengshangpinRecommend[2].shangpintupian.split(',')[0]" alt="" />
				<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-else :src="baseUrl + (shangchengshangpinRecommend[2].shangpintupian?shangchengshangpinRecommend[2].shangpintupian.split(',')[0]:'')" alt="" />
				<div class="title line1" :style='{"color":"#fff","left":"0","textAlign":"center","bottom":"0","background":"rgba(0,0,0,.3)","width":"100%","lineHeight":"44px","fontSize":"18px","position":"absolute"}'>
                    <div>{{shangchengshangpinRecommend[2].shangpinmingcheng}}</div>
                    <div>{{shangchengshangpinRecommend[2].shangpinzhonglei}}</div>
                    <div>{{shangchengshangpinRecommend[2].dianpuming}}</div>
                </div>
			</div>
		</div>
		<div class="list-body" :style='{"width":"48%","margin":"10px 0 0","float":"right","justifyContent":"space-between","display":"flex","height":"275px"}'>
			<div v-if="shangchengshangpinRecommend.length>3" @click="toDetail('shangchengshangpinDetail', shangchengshangpinRecommend[3])" class="list-item animation-box" :style='{"width":"48%","margin":"0 0px","position":"relative","display":"inline-block","height":"100%"}'>
				<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-if="preHttp(shangchengshangpinRecommend[3].shangpintupian)" :src="shangchengshangpinRecommend[3].shangpintupian.split(',')[0]" alt="" />
				<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-else :src="baseUrl + (shangchengshangpinRecommend[3].shangpintupian?shangchengshangpinRecommend[3].shangpintupian.split(',')[0]:'')" alt="" />
				<div class="title line1" :style='{"color":"#fff","left":"0","textAlign":"center","bottom":"0","background":"rgba(0,0,0,.3)","width":"100%","lineHeight":"44px","fontSize":"18px","position":"absolute"}'>
                    <div>{{shangchengshangpinRecommend[3].shangpinmingcheng}}</div>
                    <div>{{shangchengshangpinRecommend[3].shangpinzhonglei}}</div>
                    <div>{{shangchengshangpinRecommend[3].dianpuming}}</div>
                </div>
			</div>
			<div v-if="shangchengshangpinRecommend.length>4" @click="toDetail('shangchengshangpinDetail', shangchengshangpinRecommend[4])" class="list-item animation-box" :style='{"width":"48%","margin":"0 0px","position":"relative","display":"inline-block","height":"100%"}'>
				<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-if="preHttp(shangchengshangpinRecommend[4].shangpintupian)" :src="shangchengshangpinRecommend[4].shangpintupian.split(',')[0]" alt="" />
				<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-else :src="baseUrl + (shangchengshangpinRecommend[4].shangpintupian?shangchengshangpinRecommend[4].shangpintupian.split(',')[0]:'')" alt="" />
				<div class="title line1" :style='{"color":"#fff","left":"0","textAlign":"center","bottom":"0","background":"rgba(0,0,0,.3)","width":"100%","lineHeight":"44px","fontSize":"18px","position":"absolute"}'>
                    <div>{{shangchengshangpinRecommend[4].shangpinmingcheng}}</div>
                    <div>{{shangchengshangpinRecommend[4].shangpinzhonglei}}</div>
                    <div>{{shangchengshangpinRecommend[4].dianpuming}}</div>
                </div>
			</div>
		</div>
	</div>
	
	
	
	
	
	
	<div @click="moreBtn('shangchengshangpin')" :style='{"border":"1px solid #999","padding":"0 16px","margin":"20px auto 0px","top":"30px","textAlign":"center","background":"none","display":"inline-block","width":"auto","lineHeight":"30px","position":"absolute","right":"7%"}'>
		<span :style='{"color":"#202020","fontSize":"14px"}'>查看更多</span>
		<i v-if="true" :style='{"color":"#202020","fontSize":"14px"}' class="el-icon-d-arrow-right"></i>
	</div>
	
</div>


	<!-- 系统简介 -->
	<div :style='{"padding":"120px 7% 120px","margin":"0px auto 0px","flexWrap":"wrap","background":"url(http://codegen.caihongy.cn/20230109/5ffc803e6682418eb7f0b09a98e35527.png) no-repeat center top,url(http://codegen.caihongy.cn/20230109/138a4d606eae4a168810cef229969885.png) no-repeat center bottom,#fff","display":"flex","width":"100%","position":"relative","height":"auto"}'>
	  <div :style='{"margin":"-60px auto 0px","color":"#202020","textAlign":"left","background":"url(http://codegen.caihongy.cn/20230108/be8ab030ca3b48cf846466a6aefc3df7.png) no-repeat center bottom","width":"100%","lineHeight":"24px","fontSize":"20px","fontWeight":"600"}'>{{systemIntroductionDetail.title}}</div>
	  <div :style='{"width":"100%","margin":"-34px 0 20px","lineHeight":"24px","fontSize":"16px","color":"#202020","textAlign":"left"}'>{{systemIntroductionDetail.subtitle}}</div>
	  <div :style='{"width":"100%","padding":"0 0px","flexWrap":"wrap","justifyContent":"space-between","display":"flex","height":"auto"}'>
	    <img :style='{"width":"48%","margin":"0 0px","objectFit":"cover","display":"block","height":"360px"}' :src="baseUrl + systemIntroductionDetail.picture1">
	    <img :style='{"margin":"0 10px","objectFit":"cover","display":"none","height":"150px"}' :src="baseUrl + systemIntroductionDetail.picture2">
	    <img :style='{"margin":"0 10px","objectFit":"cover","flex":1,"display":"none","height":"120px"}' :src="baseUrl + systemIntroductionDetail.picture3">
	  </div>
	  <div :style='{"padding":"10px","margin":"0 0 10px 0","color":"rgb(102, 102, 102)","right":"7%","textIndent":"2em","overflow":"hidden","top":"130px","background":"#fff","width":"calc(43% - 0px)","lineHeight":"2","fontSize":"15px","position":"absolute","height":"360px"}' v-html="systemIntroductionDetail.content"></div>
	  <div :style='{"width":"285px","background":"url(\"http://codegen.caihongy.cn/20201114/7856ba26477849ea828f481fa2773a95.jpg\") 0% 0% / cover no-repeat","display":"none","height":"100px"}' />
	  <div :style='{"width":"285px","background":"url(\"http://codegen.caihongy.cn/20201114/7856ba26477849ea828f481fa2773a95.jpg\") 0% 0% / cover no-repeat","display":"none","height":"100px"}' />
	  <div :style='{"width":"285px","background":"url(\"http://codegen.caihongy.cn/20201114/7856ba26477849ea828f481fa2773a95.jpg\") 0% 0% / cover no-repeat","display":"none","height":"100px"}' />
	  <div :style='{"width":"285px","background":"url(\"http://codegen.caihongy.cn/20201114/7856ba26477849ea828f481fa2773a95.jpg\") 0% 0% / cover no-repeat","display":"none","height":"100px"}' />
	</div>

<div class="lists" :style='{"width":"100%","margin":"0px auto","position":"relative","background":"#faf0e6"}'>
	
	<div class="title" :style='{"width":"100%","padding":"0px 7%","margin":"0px auto 0px","lineHeight":"54px","textAlign":"left","background":"none"}'>
	  <span :style='{"margin":"0 4px 0 0","fontSize":"20px","lineHeight":"24px","color":"#202020","fontWeight":"bold"}'>商城商品展示</span>
	</div>
	
	<div v-if="true" class="idea" :style='{"width":"100%","padding":"0px 7%","flexWrap":"wrap","background":"#faf0e6","justifyContent":"space-between","display":"flex"}'>
		<div class="box1" :style='{"width":"100%","background":"url(http://codegen.caihongy.cn/20230110/80e36442864b4158aae8264689c04a4d.jpg) no-repeat center center / 100% 100%","height":"280px"}'></div>
		<div class="box2" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box3" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box4" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box5" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box6" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box7" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box8" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box9" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box10" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
	</div>
	
	
	
	
	
	
	
	<!-- 样式七 -->
	<div class="list list7 index-pv1" :style='{"padding":"20px 7% 40px","flexWrap":"wrap","background":"none","display":"flex","width":"100%","justifyContent":"space-between","height":"auto"}'>
		<div v-if="shangchengshangpinList.length>0" class="list-4-item animation-box item-1" @click="toDetail('shangchengshangpinDetail', shangchengshangpinList[0])" :style='{"width":"24%","margin":"0 0px","overflow":"hidden","position":"relative","height":"570px"}'>
			<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-if="preHttp(shangchengshangpinList[0].shangpintupian)" :src="shangchengshangpinList[0].shangpintupian.split(',')[0]" alt="" />
			<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-else :src="baseUrl + (shangchengshangpinList[0].shangpintupian?shangchengshangpinList[0].shangpintupian.split(',')[0]:'')" alt="" />
			<div class="list-4-item-title line1" :style='{"overflow":"hidden","color":"#fff","left":"0","textAlign":"center","bottom":"0","background":"rgba(0,0,0,.3)","width":"100%","lineHeight":"44px","fontSize":"16px","position":"absolute"}'>
                <div>{{shangchengshangpinList[0].shangpinmingcheng}}</div>
                <div>{{shangchengshangpinList[0].shangpinzhonglei}}</div>
                <div>{{shangchengshangpinList[0].dianpuming}}</div>
            </div>
		</div>
		<div :style='{"width":"24%","margin":"0 0px","height":"275px"}' class="list-4-body">
			<div v-if="shangchengshangpinList.length>1" @click="toDetail('shangchengshangpinDetail', shangchengshangpinList[1])" class="list-4-item animation-box item-2" :style='{"width":"100%","margin":"0 0 20px","position":"relative","height":"100%"}'>
				<img :style='{"width":"100%","overflow":"hidden","objectFit":"cover","float":"left","height":"100%"}' v-if="preHttp(shangchengshangpinList[1].shangpintupian)" :src="shangchengshangpinList[1].shangpintupian.split(',')[0]" alt="" />
				<img :style='{"width":"100%","overflow":"hidden","objectFit":"cover","float":"left","height":"100%"}' v-else :src="baseUrl + (shangchengshangpinList[1].shangpintupian?shangchengshangpinList[1].shangpintupian.split(',')[0]:'')" alt="" />
				<div class="list-4-item-title line1" :style='{"color":"#fff","left":"0","textAlign":"center","bottom":"0","background":"rgba(0,0,0,.3)","width":"100%","lineHeight":"44px","fontSize":"16px","position":"absolute"}'>
                    <div>{{shangchengshangpinList[1].shangpinmingcheng}}</div>
                    <div>{{shangchengshangpinList[1].shangpinzhonglei}}</div>
                    <div>{{shangchengshangpinList[1].dianpuming}}</div>
                </div>
			</div>
			<div v-if="shangchengshangpinList.length>2" @click="toDetail('shangchengshangpinDetail', shangchengshangpinList[2])" class="list-4-item animation-box item-3" :style='{"width":"100%","margin":"20px 0 0","overflow":"hidden","position":"relative","height":"100%"}'>
				<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-if="preHttp(shangchengshangpinList[2].shangpintupian)" :src="shangchengshangpinList[2].shangpintupian.split(',')[0]" alt="" />
				<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-else :src="baseUrl + (shangchengshangpinList[2].shangpintupian?shangchengshangpinList[2].shangpintupian.split(',')[0]:'')" alt="" />
				<div class="list-4-item-title line1" :style='{"color":"#fff","left":"0","textAlign":"center","bottom":"0","background":"rgba(0,0,0,.3)","width":"100%","lineHeight":"44px","fontSize":"16px","position":"absolute"}'>
                    <div>{{shangchengshangpinList[2].shangpinmingcheng}}</div>
                    <div>{{shangchengshangpinList[2].shangpinzhonglei}}</div>
                    <div>{{shangchengshangpinList[2].dianpuming}}</div>
                </div>
			</div>
		</div>
		<div v-if="shangchengshangpinList.length>3" class="list-4-item animation-box item-1" @click="toDetail('shangchengshangpinDetail', shangchengshangpinList[3])" :style='{"width":"24%","margin":"0 0px","overflow":"hidden","position":"relative","height":"570px"}'>
			<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-if="preHttp(shangchengshangpinList[3].shangpintupian)" :src="shangchengshangpinList[3].shangpintupian.split(',')[0]" alt="" />
			<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-else :src="baseUrl + (shangchengshangpinList[3].shangpintupian?shangchengshangpinList[3].shangpintupian.split(',')[0]:'')" alt="" />
			<div class="list-4-item-title line1" :style='{"color":"#fff","left":"0","textAlign":"center","bottom":"0","background":"rgba(0,0,0,.3)","width":"100%","lineHeight":"44px","fontSize":"16px","position":"absolute"}'>
                <div>{{shangchengshangpinList[3].shangpinmingcheng}}</div>
                <div>{{shangchengshangpinList[3].shangpinzhonglei}}</div>
                <div>{{shangchengshangpinList[3].dianpuming}}</div>
            </div>
		</div>
		<div :style='{"width":"24%","margin":"0 10px","height":"275px"}' class="list-4-body">
			<div v-if="shangchengshangpinList.length>4" @click="toDetail('shangchengshangpinDetail', shangchengshangpinList[4])" class="list-4-item animation-box item-4" :style='{"width":"100%","margin":"0 0 20px","overflow":"hidden","position":"relative","height":"100%"}'>
				<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-if="preHttp(shangchengshangpinList[4].shangpintupian)" :src="shangchengshangpinList[4].shangpintupian.split(',')[0]" alt="" />
				<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-else :src="baseUrl + (shangchengshangpinList[4].shangpintupian?shangchengshangpinList[4].shangpintupian.split(',')[0]:'')" alt="" />
				<div class="list-4-item-title line1" :style='{"color":"#fff","left":"0","textAlign":"center","bottom":"0","background":"rgba(0,0,0,.3)","width":"100%","lineHeight":"44px","fontSize":"16px","position":"absolute"}'>
                    <div>{{shangchengshangpinList[4].shangpinmingcheng}}</div>
                    <div>{{shangchengshangpinList[4].shangpinzhonglei}}</div>
                    <div>{{shangchengshangpinList[4].dianpuming}}</div>
                </div>
			</div>
			<div v-if="shangchengshangpinList.length>5" @click="toDetail('shangchengshangpinDetail', shangchengshangpinList[5])" class="list-4-item animation-box item-5" :style='{"width":"100%","margin":"20px 0 0","overflow":"hidden","position":"relative","height":"100%"}'>
				<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-if="preHttp(shangchengshangpinList[5].shangpintupian)" :src="shangchengshangpinList[5].shangpintupian.split(',')[0]" alt="" />
				<img :style='{"width":"100%","objectFit":"cover","float":"left","height":"100%"}' v-else :src="baseUrl + (shangchengshangpinList[5].shangpintupian?shangchengshangpinList[5].shangpintupian.split(',')[0]:'')" alt="" />
				<div class="list-4-item-title line1" :style='{"color":"#fff","left":"0","textAlign":"center","bottom":"0","background":"rgba(0,0,0,.3)","width":"100%","lineHeight":"44px","fontSize":"16px","position":"absolute"}'>
                    <div>{{shangchengshangpinList[5].shangpinmingcheng}}</div>
                    <div>{{shangchengshangpinList[5].shangpinzhonglei}}</div>
                    <div>{{shangchengshangpinList[5].dianpuming}}</div>
                </div>
			</div>
		</div>
	</div>
	
	
	
	<div @click="moreBtn('shangchengshangpin')" :style='{"border":"0","padding":"0 16px","margin":"0px auto 0px","top":"0px","textAlign":"center","background":"none","display":"inline-block","width":"auto","lineHeight":"30px","position":"absolute","right":"7%"}'>
		<span :style='{"color":"#333","fontSize":"14px"}'>查看更多</span>
		<i v-if="true" :style='{"color":"#333","fontSize":"14px"}' class="el-icon-d-arrow-right"></i>
	</div>
	

</div>

	
<div class="news" :style='{"minHeight":"520px","padding":"100px 0 20px","margin":"0px auto 0px","flexWrap":"wrap","background":"url(http://codegen.caihongy.cn/20230109/5ffc803e6682418eb7f0b09a98e35527.png) no-repeat center top,#fff","display":"flex","width":"100%","position":"relative"}'>
	
	<div class="title" :style='{"width":"100%","padding":"0px 7%","margin":"0px auto 0px","lineHeight":"54px","textAlign":"left","background":"none"}'>
		<span :style='{"margin":"0 4px 0 0","fontSize":"20px","lineHeight":"24px","color":"#202020","fontWeight":"bold"}'>商城公告</span>
	</div>
	
	<div v-if="true" class="idea newsIdea" :style='{"width":"100%","padding":"0px 7%","flexWrap":"wrap","background":"#fff","justifyContent":"space-between","display":"flex"}'>
		<div class="box1" :style='{"width":"100%","background":"url(http://codegen.caihongy.cn/20230110/533c6403944f4524a04473dbecdf6668.jpg) no-repeat center center / 100% 100%","height":"280px"}'></div>
		<div class="box2" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box3" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box4" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box5" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box6" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box7" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box8" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box9" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box10" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
	</div>
	
	
	
	
	
	
	
	
	
	
	<!-- 样式十 -->
	<div v-if="newsList.length" class="list list10 index-pv1" :style='{"padding":"40px 7% 40px","flexWrap":"wrap","background":"none","display":"flex","width":"100%","justifyContent":"space-between","height":"auto"}'>
	  <div v-if="newsList.length>0" @click="toDetail('newsDetail', newsList[0])" :style='{"width":"48%","margin":"0 0px","position":"relative","background":"none","height":"auto"}' class="new10-list-item animation-box">
	    <img :style='{"border":"6px solid #cca162","width":"100%","objectFit":"cover","display":"block","height":"220px"}' :src="baseUrl + newsList[0].picture" alt="">
		<div :style='{"width":"calc(100% - 80px)","padding":"16px 0px 8px","fontSize":"20px","lineHeight":"28px","color":"#b58339"}' class="new9-list-item-title line1">{{newsList[0].title}}</div>
		<div :style='{"padding":"4px 8px","fontSize":"12px","lineHeight":"24px","color":"#fff","background":"#cca162","display":"inline-block"}' class="new9-list-item-time">{{newsList[0].addtime.split(' ')[0]}}</div>
	    <div :style='{"padding":"0 10px","overflow":"hidden","color":"#555","fontSize":"14px","lineHeight":"24px","textIndent":"2em","height":"72px"}' class="new9-list-item-descript line2">{{newsList[0].introduction}}</div>
		<div :style='{"padding":"0 10px","margin":"0 10px 10px","color":"#999","background":"#fff","display":"none","fontSize":"12px","lineHeight":"24px"}' class="new9-list-item-identification">新闻动态</div>
	  </div>
	  <div v-if="newsList.length>1" :style='{"padding":"0 0 0 120px","margin":"0 0px","background":"url(http://codegen.caihongy.cn/20230109/558d6ae97f424b9486bb076db9173c9b.png) no-repeat left top","flexDirection":"column","display":"block","width":"48%","position":"relative","justifyContent":"space-between","height":"400px"}'>
	    <div v-for="(item,index) in newsList" v-if="index<4 && index>0" :key="index" @click="toDetail('newsDetail', item)" :style='{"width":"100%","margin":"0 0 55px","position":"relative","background":"none","height":"100px"}' class="new10-list-item animation-box">
	        <div :style='{"padding":"0px","whiteSpace":"nowrap","overflow":"hidden","color":"#b58339","width":"calc(100% - 80px)","fontSize":"20px","lineHeight":"1","textOverflow":"ellipsis"}' class="new9-list-item-title line1">{{ item.title }}</div>
	        <div :style='{"fontSize":"12px","lineHeight":"1","position":"absolute","right":"20px","color":"#b89e66","top":"2px"}' class="new9-list-item-time">{{ item.addtime.split(' ')[0] }}</div>
			<div :style='{"padding":"0 0px","margin":"5px auto 0","overflow":"hidden","color":"#555","width":"calc(100% - 0px)","fontSize":"14px","lineHeight":"24px","textIndent":"2em","height":"72px"}' class="new9-list-item-descript line2">{{ item.introduction }}</div>
			<div :style='{"padding":"0 10px","fontSize":"12px","lineHeight":"24px","color":"#999","background":"#fff","display":"none"}' class="new9-list-item-identification">新闻动态</div>
	    </div>
	  </div>
	</div>
	
	<div @click="moreBtn('news')" :style='{"border":"1px solid #999","padding":"0 16px","margin":"0px auto 0px","top":"100px","textAlign":"center","background":"none","display":"inline-block","width":"auto","lineHeight":"30px","position":"absolute","right":"7%"}'>
		<span :style='{"color":"#333","fontSize":"14px"}'>查看更多</span>
		<i v-if="true" :style='{"color":"#333","fontSize":"14px"}' class="el-icon-d-arrow-right"></i>
	</div>
	
</div>

</div>
</template>

<script>
  export default {
    //数据集合
    data() {
      return {
        baseUrl: '',
        aboutUsDetail: {},
        systemIntroductionDetail: {},
        newsList: [],
        shangchengshangpinRecommend: [],

        shangchengshangpinList: [],
      }
    },
    created() {
      this.baseUrl = this.$config.baseUrl;
      this.getNewsList();
      this.getAboutUs();
      this.getSystemIntroduction();
      this.getList();
    },
    //方法集合
    methods: {
      preHttp(str) {
          return str && str.substr(0,4)=='http';
      },
      getAboutUs() {
          this.$http.get('aboutus/detail/1', {}).then(res => {
            if(res.data.code == 0) {
              this.aboutUsDetail = res.data.data;
            }
          })
      },
      getSystemIntroduction() {
          this.$http.get('systemintro/detail/1', {}).then(res => {
            if(res.data.code == 0) {
              this.systemIntroductionDetail = res.data.data;
            }
          })
      },
		getNewsList() {
			this.$http.get('news/list', {params: {
				page: 1,
				limit: 4,
			order: 'desc'}}).then(res => {
				if (res.data.code == 0) {
					this.newsList = res.data.data.list;
					
					
				}
			});
		},
		getList() {
          let autoSortUrl = "";
          autoSortUrl = "shangchengshangpin/autoSort";
          if(localStorage.getItem('Token')) {
              autoSortUrl = "shangchengshangpin/autoSort2";
          }
			this.$http.get(autoSortUrl, {params: {
				page: 1,
				limit: 8,
			}}).then(res => {
				if (res.data.code == 0) {
					this.shangchengshangpinRecommend = res.data.data.list;
					
					
					// 商品列表样式五
					
				}
			});
			
			this.$http.get('shangchengshangpin/list', {params: {
				page: 1,
				limit: 6,
			}}).then(res => {
				if (res.data.code == 0) {
					this.shangchengshangpinList = res.data.data.list;
					
					// 商品列表样式五
					
				}
			});
		},
		toDetail(path, item) {
			this.$router.push({path: '/index/' + path, query: {detailObj: JSON.stringify(item)}});
		},
		moreBtn(path) {
			this.$router.push({path: '/index/' + path});
		}
    }
  }
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
	.home-preview {
	
		.recommend {
			.list3 .swiper-button-prev {
				left: 10px;
				right: auto;
			}
			
			.list3 .swiper-button-prev::after {
				color: rgb(64, 158, 255);
			}
			
			.list3 .swiper-button-next {
				left: auto;
				right: 10px;
			}
			
			.list3 .swiper-button-next::after {
				color: rgb(64, 158, 255);
			}
			
			.list5 .swiper-button-prev {
				left: 10px;
				right: auto;
			}
			
			.list5 .swiper-button-prev::after {
				color: rgb(64, 158, 255);
        }
        
        .list5 .swiper-button-next {
				left: auto;
				right: 10px;
			}
			
			.list5 .swiper-button-next::after {
				color: rgb(64, 158, 255);
			}
			
			.list5 {
				.swiper-slide-prev {
					position: relative;
					z-index: 3;
				}
		
				.swiper-slide-next {
					position: relative;
					z-index: 3;
				}
		
				.swiper-slide-active {
					position: relative;
					z-index: 5;
				}
			}
			
			.index-pv1 .animation-box {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
				z-index: initial;
			}
			
			.index-pv1 .animation-box:hover {
				transform: translate3d(0px, 10px, 0px);
				-webkit-perspective: 1000px;
				perspective: 1000px;
				transition: 0.3s;
				z-index: 1;
			}
			
			.index-pv1 .animation-box img {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
			}
			
			.index-pv1 .animation-box img:hover {
				-webkit-perspective: 1000px;
				perspective: 1000px;
				transition: 0.3s;
			}
		}
		
		.news {
			.list3 .swiper-button-prev {
				left: 10px;
				right: auto;
			}
			
			.list3 .swiper-button-prev::after {
				color: rgb(64, 158, 255);
			}
			
			.list3 .swiper-button-next {
				left: auto;
				right: 10px;
			}
			
			.list3 .swiper-button-next::after {
				color: rgb(64, 158, 255);
			}
			
			.list6 .swiper-button-prev {
				left: 10px;
				right: auto;
			}
			
			.list6 .swiper-button-prev::after {
				color: rgb(64, 158, 255);
			}
			
			.list6 .swiper-button-next {
				left: auto;
				right: 10px;
			}
			
			.list6 .swiper-button-next::after {
				color: rgb(64, 158, 255);
			}
			
			.index-pv1 .animation-box {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
				z-index: initial;
			}
			
			.index-pv1 .animation-box:hover {
				transform: translate3d(10px,0px, 0px);
				-webkit-perspective: 1000px;
				perspective: 1000px;
				transition: 0.3s;
				z-index: 1;
			}
			
			.index-pv1 .animation-box img {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
			}
			
			.index-pv1 .animation-box img:hover {
				-webkit-perspective: 1000px;
				perspective: 1000px;
				transition: 0.3s;
			}
		}
	
		.lists {
			.list3 .swiper-button-prev {
				left: 10px;
				right: auto;
			}
			
			.list3 .swiper-button-prev::after {
				color: rgb(64, 158, 255);
			}
			
			.list3 .swiper-button-next {
				left: auto;
				right: 10px;
        }
        
        .list3 .swiper-button-next::after {
				color: rgb(64, 158, 255);
			}
			
			.list5 .swiper-button-prev {
				left: 10px;
				right: auto;
			}
			
			.list5 .swiper-button-prev::after {
				color: rgb(64, 158, 255);
			}
			
			.list5 .swiper-button-next {
            left: auto;
            right: 10px;
			}
			
			.list5 .swiper-button-next::after {
				color: rgb(64, 158, 255);
			}
			
			.list5 {
				.swiper-slide-prev {
					position: relative;
					z-index: 3;
				}
		
				.swiper-slide-next {
					position: relative;
					z-index: 3;
				}
		
				.swiper-slide-active {
					position: relative;
					z-index: 5;
				}
			}
			
			.index-pv1 .animation-box {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
				z-index: initial;
			}
			
			.index-pv1 .animation-box:hover {
				transform: translate3d(0px, 10px, 0px);
				-webkit-perspective: 1000px;
				perspective: 1000px;
				transition: 0.3s;
				z-index: 1;
			}
			
			.index-pv1 .animation-box img {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
			}
			
			.index-pv1 .animation-box img:hover {
				-webkit-perspective: 1000px;
				perspective: 1000px;
				transition: 0.3s;
			}
		}
	}
</style>
