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
import { toJSON, config } from './config';
import Card from '@mybricks/comlib-pc-normal/es/Card';
import Toolbar from '@mybricks/comlib-pc-normal/es/Toolbar';
import Link from '@mybricks/comlib-pc-normal/es/Link';
import Text from '@mybricks/comlib-pc-normal/es/Text';

export default defineComponent<{ title: string }>({
  components: {
    Renderer: RendererComponent,
  },
  emits: {},
  defineExpose: ['cat1', 'cat2'],
  setup(props, ctx) {
    const _comRef = ref();
    const _show = ref(false);

    return {
      _comRef,
      _show,
      _childProps: {},
      _config: config,
      _json: toJSON,
      _comDefs: {
        'mybricks.normal-pc.card': { runtime: Card },
        'mybricks.normal-pc.toolbar': { runtime: Toolbar },
        'mybricks.normal-pc.link': { runtime: Link },
        'mybricks.normal-pc.text': { runtime: Text },
      },
    };
  },
  methods: {
    cat1(params: string) {
      this._getRef(params, 'cat1', null).then((ref) => {
        ref.cat1(params);
      });
    },
    cat2(params: string) {
      this._getRef(params, 'cat2', null).then((ref) => {
        ref.cat2(params);
      });
    },

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
