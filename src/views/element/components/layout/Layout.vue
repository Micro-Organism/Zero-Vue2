<!--
 * @Author: Micro-Organism
 * @Date: 2024/8/26 14:36
 * @FilePath: src\views\element\components\layout\Layout.vue
 * @Email: coolrabbit1993@gmail.com
 * @Description: Layout 通过基础的 24 分栏，迅速简便地创建布局。
-->
<template>
  <div>
    <!--  基础布局 使用单一分栏创建基础的栅格布局 -->
    <!--  通过 row 和 col 组件，并通过 col 组件的 span 属性我们就可以自由地组合布局  -->
    <el-container class="container">
      <p>基础布局 使用单一分栏创建基础的栅格布局</p>
      <el-row>
        <el-col :span="24">
          <div class="grid-content bg-purple-dark">
            <div class="self-div"><p>24: 1段式</p></div>
          </div>
        </el-col>
      </el-row>
      <el-row>
        <el-col :span="12">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>12: 2段式</p></div>
          </div>
        </el-col>
        <el-col :span="12">
          <div class="grid-content bg-purple-light">
            <div class="self-div"><p>12: 2段式</p></div>
          </div>
        </el-col>
      </el-row>
      <el-row>
        <el-col :span="8">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>8: 3段式</p></div>
          </div>
        </el-col>
        <el-col :span="8">
          <div class="grid-content bg-purple-light">
            <div class="self-div"><p>8: 3段式</p></div>
          </div>
        </el-col>
        <el-col :span="8">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>8: 3段式</p></div>
          </div>
        </el-col>
      </el-row>
      <el-row>
        <el-col :span="6">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>6: 4段式</p></div>
          </div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple-light">
            <div class="self-div"><p>6: 4段式</p></div>
          </div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>6: 4段式</p></div>
          </div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple-light">
            <div class="self-div"><p>6: 4段式</p></div>
          </div>
        </el-col>
      </el-row>
      <el-row>
        <el-col :span="4">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>4: 6段式</p></div>
          </div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple-light">
            <div class="self-div"><p>4: 6段式</p></div>
          </div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>4: 6段式</p></div>
          </div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple-light">
            <div class="self-div"><p>4: 6段式</p></div>
          </div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>4: 6段式</p></div>
          </div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple-light">
            <div class="self-div"><p>4: 6段式</p></div>
          </div>
        </el-col>
      </el-row>
    </el-container>

    <!--  分栏间隔  -->
    <!--  Row 组件 提供 gutter 属性来指定每一栏之间的间隔，默认间隔为 0。  -->
    <el-container class="container">
      <p>分栏间隔 Row 组件提供 gutter 属性来指定每一栏之间的间隔，默认间隔为 0</p>
      <el-row :gutter="10">
        <el-col :span="6">
          <div class="grid-content bg-purple">
              <div class="self-div"><p>6: 4段式</p></div>
          </div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple-light">
            <div class="self-div"><p>6: 4段式</p></div>
          </div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>6: 4段式</p></div>
          </div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>6: 4段式</p></div>
          </div>
        </el-col>
      </el-row>
    </el-container>

    <!--  混合布局  -->
    <!--  通过基础的 1/24 分栏任意扩展组合形成较为复杂的混合布局。  -->
    <el-container class="container">
      <p>混合布局 通过基础的 1/24 分栏任意扩展组合形成较为复杂的混合布局。</p>
      <el-row :gutter="20">
        <el-col :span="16">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>16</p></div>
          </div>
        </el-col>
        <el-col :span="8">
          <div class="grid-content bg-purple-light">
            <div class="self-div"><p>8</p></div>
          </div>
        </el-col>
      </el-row>
      <el-row :gutter="20">
        <el-col :span="8">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>8</p></div>
          </div>
        </el-col>
        <el-col :span="8">
          <div class="grid-content bg-purple-light">
            <div class="self-div"><p>8</p></div>
          </div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>4</p></div>
          </div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>4</p></div>
          </div>
        </el-col>
      </el-row>
      <el-row :gutter="20">
        <el-col :span="4">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>4</p></div>
          </div>
        </el-col>
        <el-col :span="16">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>16</p></div>
          </div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple">
            <div class="self-div"><p>4</p></div>
          </div>
        </el-col>
      </el-row>
    </el-container>

    <!--  分栏偏移  -->
    <!--  支持偏移指定的栏数。 通过制定 col 组件的 offset 属性可以指定分栏偏移的栏数。 -->
    <el-container class="container">
      <p>分栏偏移 支持偏移指定的栏数。 通过制定 col 组件的 offset 属性可以指定分栏偏移的栏数</p>
      <el-row :gutter="20">
        <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
        <el-col :span="6" :offset="6"><div class="grid-content bg-purple"></div></el-col>
      </el-row>
      <el-row :gutter="20">
        <el-col :span="6" :offset="6"><div class="grid-content bg-purple"></div></el-col>
        <el-col :span="6" :offset="6"><div class="grid-content bg-purple"></div></el-col>
      </el-row>
      <el-row :gutter="20">
        <el-col :span="12" :offset="6"><div class="grid-content bg-purple"></div></el-col>
      </el-row>
    </el-container>

    <!--  对齐方式  -->
    <!--  通过 flex 布局来对分栏进行灵活的对齐。 -->
    <!--  将 type 属性赋值为 'flex'，可以启用 flex 布局，并可通过 justify 属性来指定 start, center, end, space-between, space-around 其中的值来定义子元素的排版方式。  -->
    <el-container class="container">
      <p>对齐方式 通过 flex 布局来对分栏进行灵活的对齐。</p>
      <el-row type="flex" class="row-bg">
        <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
        <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
        <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      </el-row>
      <el-row type="flex" class="row-bg" justify="center">
        <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
        <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
        <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      </el-row>
      <el-row type="flex" class="row-bg" justify="end">
        <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
        <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
        <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      </el-row>
      <el-row type="flex" class="row-bg" justify="space-between">
        <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
        <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
        <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      </el-row>
      <el-row type="flex" class="row-bg" justify="space-around">
        <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
        <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
        <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      </el-row>
    </el-container>

    <!--  响应式布局  -->
    <!--  参照了 Bootstrap 的 响应式设计，预设了五个响应尺寸：xs、sm、md、lg 和 xl。  -->
    <el-container class="container">
      <p>响应式布局  参照了 Bootstrap 的 响应式设计，预设了五个响应尺寸：xs、sm、md、lg 和 xl。</p>
      <el-row :gutter="10">
        <el-col :xs="8" :sm="6" :md="4" :lg="3" :xl="1"><div class="grid-content bg-purple"></div></el-col>
        <el-col :xs="4" :sm="6" :md="8" :lg="9" :xl="11"><div class="grid-content bg-purple-light"></div></el-col>
        <el-col :xs="4" :sm="6" :md="8" :lg="9" :xl="11"><div class="grid-content bg-purple"></div></el-col>
        <el-col :xs="8" :sm="6" :md="4" :lg="3" :xl="1"><div class="grid-content bg-purple-light"></div></el-col>
      </el-row>
    </el-container>
  </div>
</template>

<script>

</script>

<style scoped lang="scss">
.container {
  display: flex;
  justify-content: center; /* 水平居中 */
  flex-direction: column; /* 垂直居中 */
  margin: 2rem;
  .self-div {
    display: flex;
    justify-content: center; /* 水平居中 */
    align-items: center; /* 垂直居中 */
    //height: 100vh; /* 使用视口高度 */
  }
}

.el-row {
  margin-bottom: 20px;

  &:last-child {
    margin-bottom: 0;
  }
}

.el-col {
  border-radius: 4px;
}

.bg-purple-dark {
  background: #99a9bf;
}

.bg-purple {
  background: #d3dce6;
}

.bg-purple-light {
  background: #e5e9f2;
}

.grid-content {
  border-radius: 4px;
  min-height: 36px;
}

.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
</style>
