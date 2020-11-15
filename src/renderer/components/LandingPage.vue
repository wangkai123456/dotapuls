<template>
  <div class="box">
    <div class="table-item">
      <div>总体数据</div>
      <el-table
        border
        :data="tableData"
        style="width: 100%;height:100%;margin-top: 10px;"
      >
        <el-table-column prop="name" label="玩家"> </el-table-column>
        <el-table-column prop="skill" label="段位"> </el-table-column>
        <el-table-column prop="address" label="总比赛">
          <template>
            <div class="min-hgi">5000 (54%)</div>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="table-item">
      <div>当月数据</div>
      <el-table border :data="tableData" style="width: 100%;height:100%;margin-top: 10px;">
        <el-table-column prop="address" label="总比赛"> </el-table-column>
        <el-table-column prop="date" label="最多使用英雄">
          <template>
            <img
              v-for="item in 5"
              :key="item"
              class="ava"
              :src="require('./../assets/3321605243470_.pic.jpg')"
              alt=""
            />
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="table-item no-bor">
      <div>值得注意</div>
      <img
        class="hero"
        :src="require('./../assets/3321605243470_.pic.jpg')"
        alt=""
      />
      <div class="often-hero">
        <img
          v-for="item in 4"
          :key="item"
          class="ava-2"
          :src="require('./../assets/3321605243470_.pic.jpg')"
          alt=""
        />
      </div>
      <el-carousel class="advertisement">
        <el-carousel-item v-for="item in 4" :key="item">
          <h3 class="small">美女荷官，在线发票</h3>
        </el-carousel-item>
      </el-carousel>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      loading: false,
      tableData: [
        {
          name: "噜噜噜",
          skill: "最强王者",
          address: "5000 (54%)",
        },
        {
          name: "噜噜噜",
          skill: "最强王者",
          address: "5000 (54%)",
        },
        {
          name: "噜噜噜",
          skill: "最强王者",
          address: "5000 (54%)",
        },
        {
          name: "噜噜噜",
          skill: "最强王者",
          address: "5000 (54%)",
        },
        {
          name: "噜噜噜",
          skill: "最强王者",
          address: "5000 (54%)",
        },
        {
          name: "噜噜噜",
          skill: "最强王者",
          address: "5000 (54%)",
        },
        {
          name: "噜噜噜",
          skill: "最强王者",
          address: "5000 (54%)",
        },
        {
          name: "噜噜噜",
          skill: "最强王者",
          address: "5000 (54%)",
        },
        {
          name: "噜噜噜",
          skill: "最强王者",
          address: "5000 (54%)",
        },
      ],
    };
  },
  name: "landing-page",
  methods: {
    open(link) {
      this.$electron.shell.openExternal(link);
    },
  },
};
</script>

<style scoped>
.no-bor {
  border: none;
}
.table-item {
  width: 33%;
  text-align: center;
}
.box {
  display: flex;
  width: 100%;
  height: 100%;
  justify-content: space-between;
}
.ava {
  width: 28px;
  height: 28px;
  border-radius: 28px;
  margin-right: 5px;
}
.hero {
  width: 150px;
  height: 150px;
  border-radius: 150px;
  margin-top: 10px;
}
.ava-2 {
  width: 60px;
  height: 60px;
  border-radius: 60px;
}
.often-hero {
  display: flex;
  align-items: center;
  justify-content: space-around;
}
.min-hgi {
  height: 35px;
}
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
.advertisement {
  width: 100%;
  margin-top: 20px;
  min-height: 100%;
}
</style>
