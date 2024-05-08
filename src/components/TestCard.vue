/** * 以下内容由 MyBricks 平台生成 *
地址：https://my.mybricks.world/mybricks-app-pc-cdm/index.html?id=562086822649925
*/

<template>
  <div v-if="!_show" style="width: 100%; height: 200px"></div>
  <Renderer
    v-show="_show"
    ref="_comRef"
    :props="{ ..._childProps, title }"
    :config="_config"
    :json="_json"
    :comDefs="_comDefs"
    @_my-on-mounted="() => _myOnMounted()"
  />
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue';
import RendererComponent from '@mybricks/renderer-pc/src/toVue/index.vue';
import Card from '@mybricks/comlib-pc-normal/es/Card';
import Toolbar from '@mybricks/comlib-pc-normal/es/Toolbar';

const json = {"themes":{"comThemes":{}},"global":{"comsReg":{},"consReg":{},"pinRels":{},"pinProxies":{},"fxFrames":[]},"scenes":[{"-v":"1.0.19","deps":[{"namespace":"mybricks.normal-pc.card","version":"1.0.22"},{"namespace":"mybricks.normal-pc.toolbar","version":"1.0.32"}],"coms":{"u_Y4C8Z":{"id":"u_Y4C8Z","def":{"namespace":"mybricks.normal-pc.card","version":"1.0.22"},"title":"卡片","model":{"data":{"title":"卡片","useExtra":false,"bordered":true,"hoverable":false,"cursor":false,"size":"default","style":{},"bodyStyle":{},"outputContent":0,"dataType":"number","borderStyle":{"borderRadius":"8px 8px 8px 8px","borderColor":"#F0F0F0 #F0F0F0 #F0F0F0 #F0F0F0","borderWidth":"1px 1px 1px 1px","borderStyle":"solid solid solid solid"},"isAction":false,"items":[{"key":"key1","name":"操作项1"}],"padding":"24px","isHeight":false,"height":"80px","showTitle":true,"slotStyle":{"display":"block","position":"smart","flexDirection":"column","alignItems":"flex-start","justifyContent":"flex-start","flexWrap":"nowrap","rowGap":0,"columnGap":0}},"inputAry":[],"outputAry":[],"outputEvents":{},"style":{"display":"block","left":23,"top":0,"height":196,"width":480,"widthFact":480,"heightFact":196,"position":"relative","margin":"0px 0px 0px 23px"}},"style":{"width":480,"height":196},"configs":[],"_inputs":[],"inputs":["title","show","hide","showOrHide"],"outputs":["setTitleDone"]},"u_196Jr":{"id":"u_196Jr","def":{"namespace":"mybricks.normal-pc.toolbar","version":"1.0.32"},"title":"工具条","model":{"data":{"btnList":[{"key":"btn0","text":"按钮0","showText":true,"dataType":"number","outVal":0,"inVal":"","isCustom":false,"contentSize":[14,14],"iconDistance":8,"src":"","loading":false,"useDynamicLoading":false,"style":{"height":"auto","width":"auto"},"useIcon":false},{"key":"u_x87a96","text":"按钮1","showText":true,"dataType":"number","outVal":0,"inVal":"","isCustom":false,"src":"","contentSize":[14,14],"iconDistance":8,"loading":false,"useDynamicLoading":false,"style":{"height":"auto","width":"auto"},"isSlot":false,"useIcon":false}],"layout":"flex-start","spaceSize":[4,4]},"inputAry":[],"outputAry":[{"hostId":"u_x87a96","title":"单击按钮1","schema":{"type":"number"}},{"hostId":"doubleClick_u_x87a96","title":"双击按钮1","schema":{"type":"number"}},{"hostId":"u_dy4853","title":"单击按钮2","schema":{"type":"number"}},{"hostId":"doubleClick_u_dy4853","title":"双击按钮2","schema":{"type":"number"}}],"outputEvents":{"u_x87a96":[{"type":"defined","options":{},"active":true}],"doubleClick_u_x87a96":[{"type":"defined","options":{},"active":true}],"btn0":[{"type":"defined","options":{},"active":true}],"doubleClick_btn0":[{"type":"defined","options":{},"active":true}],"u_dy4853":[{"type":"defined","options":{},"active":true}],"doubleClick_u_dy4853":[{"type":"defined","options":{},"active":true}]},"style":{"display":"flex","left":0,"top":0,"heightAuto":true,"height":"fit-content","width":200,"widthFact":200,"heightFact":32,"position":"relative","visibility":"visible","flexDirection":"column","inSmartLayout":true,"margin":"0px 0px 0px 0px"}},"style":{"width":200,"height":32},"configs":[],"_inputs":[],"inputs":["show","hide","showOrHide"],"outputs":["btn0","doubleClick_btn0","u_x87a96","doubleClick_u_x87a96","doubleClick_u_dy4853"]}},"id":"u_XVtXE","title":"组件","type":"normal","comsAutoRun":{},"_inputs":[],"_outputs":[],"inputs":[{"id":"title","title":"卡片标题","type":"config","schema":{"type":"string"},"extValues":{}}],"outputs":[],"cons":{"_rootFrame_-title":[{"id":"u_CG2UR","type":"com","frameKey":"_rootFrame_","targetFrameKey":"_rootFrame_","finishPinParentKey":"u_vbl0D","comId":"u_Y4C8Z","def":{"namespace":"mybricks.normal-pc.card","version":"1.0.22"},"pinId":"title","pinType":"normal","direction":"input"}]},"pinRels":{"u_Y4C8Z-title":["setTitleDone"]},"pinProxies":{},"pinValueProxies":{},"slot":{"id":"u_XVtXE","title":"组件","showType":"module","layoutTemplate":[{"id":"u_Y4C8Z","name":"u_rX_6X","def":{"namespace":"mybricks.normal-pc.card","version":"1.0.22"},"slots":{"body":{"id":"body","title":"卡片内容容器","layoutTemplate":[{"id":"u_196Jr","name":"u_RnDo0","def":{"namespace":"mybricks.normal-pc.toolbar","version":"1.0.32"},"brother":[],"child":null}],"comAry":[{"id":"u_196Jr","name":"u_RnDo0","def":{"namespace":"mybricks.normal-pc.toolbar","version":"1.0.32"}}],"style":{"zoom":1,"layout":"smart","justifyContent":"flex-start","alignItems":"flex-start","widthFact":430,"heightFact":87,"width":430,"height":87}}},"brother":[],"child":null}],"comAry":[{"id":"u_Y4C8Z","name":"u_rX_6X","def":{"namespace":"mybricks.normal-pc.card","version":"1.0.22"},"slots":{"body":{"id":"body","title":"卡片内容容器","layoutTemplate":[{"id":"u_196Jr","name":"u_RnDo0","def":{"namespace":"mybricks.normal-pc.toolbar","version":"1.0.32"},"brother":[],"child":null}],"comAry":[{"id":"u_196Jr","name":"u_RnDo0","def":{"namespace":"mybricks.normal-pc.toolbar","version":"1.0.32"}}],"style":{"zoom":1,"layout":"smart","justifyContent":"flex-start","alignItems":"flex-start","widthFact":430,"heightFact":87,"width":430,"height":87}}}}],"style":{"zoom":1,"layout":"smart","justifyContent":"flex-start","alignItems":"flex-start","width":509,"widthFull":true,"height":200,"heightAuto":true,"widthFact":509,"heightFact":200}}}],"plugins":{"@mybricks/plugins/service":[]},"hasPermissionFn":"(function()%20%7B%20var%20_RTFN_%3B%20%0A%22use%20strict%22%3B%0A%0A_RTFN_%20%3D%20undefined%3B%0A%3B%20return%20_RTFN_%3B%20%7D)()"}
const executeEnv = 'test';
const envList = [];
const i18nLangContent = undefined;

const getCurrentLocale = () => {
  // 当前语言
  return navigator.language;
};

export default defineComponent({
  components: {
    Renderer: RendererComponent,
  },
  props: {
    title: String,
  },
  emits: {},
  defineExpose: [],
  setup(props, ctx) {
    const _comRef = ref();
    const _show = ref(false);

    return {
      _comRef,
      _show,
      _childProps: {},
      _config: {
        executeEnv,
        envList,
        i18nLangContent,
        locale: getCurrentLocale(),
      },
      _json: json,
      _comDefs: {
        'mybricks.normal-pc.card': { runtime: Card },
        'mybricks.normal-pc.toolbar': { runtime: Toolbar },
      },
    };
  },
  methods: {
    _myOnMounted() {
      setTimeout(() => {
        this._show = true;
      }, 0);
    },
    _getRef(params, key, res) {
      return new Promise((resolve, reject) => {
        if (this._comRef.currentRef && this._comRef.currentRef[key]) {
          if (res) {
            res(this._comRef.currentRef);
          } else {
            resolve(this._comRef.currentRef);
          }
        } else {
          setTimeout(() => {
            this._getRef(params, key, res).then(() => {
              resolve(this._comRef.currentRef);
            });
          }, 0);
        }
      });
    },
  },
});
</script>

<style>
@import 'antd/dist/antd.css';
</style>
