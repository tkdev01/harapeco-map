<template>
  <v-layout>
    <v-flex class="text-center">
      <v-alert type="info">
        Mapの編集は<span class="font-weight-bold">「PC」</span>をご利用ください。<br>
        スマホからの編集には対応しておりません。m(_　_)m
      </v-alert>
      <v-card>
        <v-tabs
        background-color="gray"
        color="white accent-4"
        right
        >
          <v-tab>Mapにお店情報がある場合</v-tab>
          <v-tab>MAPにお店情報がない場合</v-tab>

          <!-- <v-tab-item
              v-for="n in 3"
              :key="n"
          > -->
          <v-tab-item>
              <v-container fluid>
                <p>Map右上の四角のマークをクリックします。</p>
                <img src="~/assets/img/howtoedit1.png" width="100%" alt="イラスト1"/>
                <p>「編集します」をクリックします。</p>
                <img src="~/assets/img/howtoedit2.png" width="100%" alt="イラスト1" />
                <p>編集画面が表示されます。</p>
                <img src="~/assets/img/howtoedit3.png" width="100%" alt="イラスト1" />
                <p>画面左側のレイヤーを選択します。</p>
                <p>※好みのレイヤーがない場合は作成することも可能です。</p>
                <br>
                <p>検索ボックスから店名を検索</p>
                <img src="~/assets/img/howtoedit7.png" width="100%" alt="イラスト1" />
                <p>「地図に追加」を押します。</p>
                <img src="~/assets/img/howtoedit8.png" width="100%" alt="イラスト1" />
                <p>もう一度場所を選択し、お店情報を編集します。</p>
                <img src="../assets/img/howtoedit9.png" width="100%" alt="イラスト1" />
                <p>お店情報を記載しましょう。</p>
                <img src="../assets/img/howtoedit10.png" width="100%" alt="イラスト1" />
                <p>
                  Mapの編集は以上です。<br>
                  ※更新が反映されるまで時間がかかる場合があります。
                </p>
              </v-container>
          </v-tab-item>
          <v-tab-item>
            <v-container fluid>
              <p>Map右上の四角のマークをクリックします。</p>
              <img src="~/assets/img/howtoedit1.png" width="100%" alt="イラスト1" />
              <p>「編集します」をクリックします。</p>
              <img src="~/assets/img/howtoedit2.png" width="100%" alt="イラスト1" />
              <p>編集画面が表示されます。</p>
              <img src="~/assets/img/howtoedit3.png" width="100%" alt="イラスト1" />

              <p>レイヤー(和・洋・中)を選択し、ピンマークを選択します。</p>
              <img src="~/assets/img/howtoedit4.png" width="100%" alt="イラスト1" />

              <p>お店の場所をクリックします。</p>
              <img src="~/assets/img/howtoedit5.png" width="100%" alt="イラスト1" />
              <p>
                定休日や店舗の広さなど役立つ情報をどんどん記載しましょう。<br>
                以上で更新は完了です。<br>
                <br>
                ※更新が反映されるまで時間がかかる場合があります。
              </p>
            </v-container>
          </v-tab-item>
        </v-tabs>
      </v-card>
    </v-flex>
  </v-layout>
</template>
<script>
export default {

}
</script>
<style lang="scss" scoped>

</style>