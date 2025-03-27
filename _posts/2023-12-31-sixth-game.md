---
title: ReVE
author: ゆうじん
layout: post
---

<iframe width="480" height="270"
src="https://www.youtube.com/embed/GeDLqBxk9n0">
</iframe>

<div class="table-wrapper">
  <table>
    <thead>
      <tr>
        <th> </th>
        <th> </th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>ジャンル</td>
        <td>ゲームエンジン</td>
      </tr>
      <tr>
        <td>制作期間</td>
        <td>3月</td>
      </tr>
      <tr>
        <td>開発環境</td>
        <td>Vulkan / C++ / VS2022</td>
      </tr>
      <tr>
        <td>制作人数</td>
        <td>個人</td>
      </tr>
      <tr>
        <td>担当</td>
        <td>全て</td>
      </tr>
    </tbody>
  </table>
</div>

<h4>
    VulkanAPIを使って、WindowsとLinuxとAndroidで動作するマルチプラットフォームでオープンワールドゲームを扱えるレンダリングエンジンを目指しています。<br>
    Unreal Engineを参考にしてフォトリアルな表現をチャレンジします。<br>
    作品はCMakeに基づいて両方プラットフォームで起動します。
  <p>
        <h4>
        <span class="image fit"><img src="{{ 'assets/images/windowslinux.png' | relative_url }}" alt="" /></span>
        </h4>
  </p>

  <p>
        <h3>完成なシーン</h3>
        <span class="image fit"><img src="{{ 'assets/images/scene2.png' | relative_url }}" alt="" /></span>
  </p>

  <p>
        <h3>レンダリングパイプライン</h3>
        <span class="image fit"><img src="{{ 'assets/images/Pipeline2.png' | relative_url }}" alt="" /></span>
  </p>

  <p>
    <span class="image left"><img src="{{ 'assets/images/pbr.jpg' | relative_url }}" alt="" /></span>
    光学的に正確なレンダリングを実現しました。たとえぱ物理的なマテリアルモデルのためにPBRは異なる種類の素材 金属、非金属、絶縁体など に対するマテリアルモデルを提供し、それぞれの物質の光学的な特性を考慮します。<br>
        サポートマテリアルはアルベド、ノーマル、ラフネス、アンビエントオクルージョン、エミッションも含めています。
  </p>

  <p>
    <span class="image left"><img src="{{ 'assets/images/cube1.jpg' | relative_url }}" alt="" /></span>
    高ダイナミックレンジの環境マップ(HDRIマップ)は、360度の環境全体を捉えた画像です。この画像は、照明情報を含む色や明るさの情報を提供します。
    IBLを使用すると、シーン内の物体は周囲の環境に基づいてリアルな反射を持つことができます。物体の表面はHDRIマップからの照明情報を利用し、周囲の環境に適切に反映されます。
  </p>

  <p>
      <span class="image left"><img src="{{ 'assets/images/transparency.jpg' | relative_url }}" alt="" /></span>
      WBOITで各ピクセルにおいて、透明なオブジェクトの深度情報を保存します。同様に、透明度情報も保存します。そして、最終的な描画時に、保存された深度と透明度情報をもとに、正確な合成を行います。これにより、重なった透明なオブジェクトが適切に描かれます。
  </p>

  <p>
      <span class="image left"><img src="{{ 'assets/images/scene.jpg' | relative_url }}" alt="" /></span>
      PCFは、シャドウマップのサンプリングを拡張してエッジの滑らかさを向上させます。具体的な手法としては、各ピクセルにおいて複数のサンプルを取り、そのサンプルの深度値を比較して影の被覆率を計算します。これにより、エッジの周りの複数のサンプルを考慮することで、柔らかい影を生成することができます。
  </p>

  <p>
      <span class="image left"><img src="{{ 'assets/images/water_flame.jpg' | relative_url }}" alt="" /></span>
      炎は特別なテクスチャにレイマーチングを行います。結果は画面に出せます。<br>
      水はUVスクロールとキューブマッパの反射で実装しています。
  </p>

  <p>
      <span class="image left"><img src="{{ 'assets/images/snow.png' | relative_url }}" alt="" /></span>
      コンピュータシェーダーで使用されます。各パーティクルに対して、位置や色、サイズなどを計算します。<br>
      重力、風、要素を組み込みます。これにより、雪のエフェクを実装します。
  </p>

</h4>


<footer>
    <a href="https://github.com/YevgeniiDimoglo/Astroworks" class="button scrolly">作品ソースコード</a>
        <a href="https://drive.google.com/file/d/1D8VOOsSH3iROdtSYOsLnI_rHxDDETQQA/view?usp=sharing" class="button scrolly">作品データ</a>
</footer>

