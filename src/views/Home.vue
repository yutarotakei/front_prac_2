<template>
  <div class="about">
    <h1>テクスト分析  </h1>

  <v-container fluid>
    <v-card elevation="0">
    <h2>テクストを手動で入力する</h2>
    <v-textarea
      name="input-7-1"
      filled
      label="テクストを手動で入力"
      auto-grow
      value=""
    ></v-textarea>
    <div class="display-4 font-weight-black text-xs-center mb-3">FOR YOUR LIFE</div>
          <div class="display-1 font-weight-bold text-xs-center">They are so cute!</div>
    </v-card>
  </v-container>
  <v-app>
  <v-card>
    <v-card-title>
      <h1 class="display-1">ログイン</h1>
    </v-card-title>
    <v-card-text>
      <v-form>
        <v-text-field label="ユーザ名" />
        <v-text-field label="パスワード" />
      </v-form>
    </v-card-text>
  </v-card>
</v-app>

  <v-container>
    <h2>ファイルをアップロードする</h2>
    <v-file-input
    accept="image/*"
    label="File input"
  ></v-file-input>
    </v-container>


  <v-container>
        <h2>相関を調べたい単語を入れる</h2>
    <v-row
      justify="space-between"
    >
      <v-col
        cols="12"
        md="4"
      >
        <v-form ref="form">
          <v-text-field
            v-model="model"
            :counter="max"
            :rules="rules"
            label="単語を入れる"
          ></v-text-field>
        </v-form>
      </v-col>
    </v-row>
  </v-container>

<v-container>
 <h2>頻出度順の写真</h2>
  <v-img
  lazy-src="https://picsum.photos/id/11/10/6"
  max-height="300"
  max-width="414"
  src="https://picsum.photos/id/11/500/300"
></v-img>
</v-container>

  </div>
</template>


<style scoped>
h1 {
  /*線の種類（二重線）太さ 色*/
  border-bottom: double 5px #FFC778;
}


</style>