<template>
  <div id="app">
    <el-container>
      <el-header style="padding: 0;">
        <Header />
      </el-header>
      <el-main>
        Nft Web
        <el-button
          type="primary"
          @click="createCollection"
        >创建合约</el-button>
      </el-main>
    </el-container>
    <CreateCollectionDialog ref="collectionDialog" />
  </div>
</template>

<script>
import Header from "@/components/header";
import CreateCollectionDialog from "@/collections/CreateCollectionDialog.vue";

export default {
  name: "App",
  components: {
    Header,
    CreateCollectionDialog,
  },
  methods: {
    createCollection() {
      this.$refs.collectionDialog.openDialog();
    },
  },
};
</script>

<style>
#app {
  background-color: #fff;
}
</style>
