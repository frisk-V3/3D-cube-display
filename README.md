3D cube display
このプロジェクトは Three.js r128 を使用して、ブラウザ上に回転する 3D キューブを描画する最小構成のサンプルです。
HTML ファイルを開くだけで動作し、追加のビルド工程は不要です。

機能概要
Three.js を CDN から読み込み

シーン・カメラ・レンダラーの基本セットアップ

ワイヤーフレーム表示の立方体を生成

requestAnimationFrame を用いたアニメーションループ

キューブが X/Y 軸方向に回転し続ける

🧩 コード構成
1. Three.js の読み込み
html
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
2. シーン・カメラ・レンダラーの初期化
THREE.Scene() でシーンを作成

THREE.PerspectiveCamera() で視点を設定

THREE.WebGLRenderer() で WebGL レンダラーを生成し、画面全体に描画

3. 立方体の作成
js
const geometry = new THREE.BoxGeometry();
const material = new THREE.MeshBasicMaterial({
    color: 0x00ff00,
    wireframe: true
});
const cube = new THREE.Mesh(geometry, material);
scene.add(cube);
4. アニメーション処理
requestAnimationFrame() でループ

毎フレームごとにキューブを回転

renderer.render(scene, camera) で描画

🚀 実行方法
この HTML ファイルを保存（例：index.html）

ブラウザで開くだけで動作
（ローカルサーバー不要）

📝 使用技術
技術	説明
Three.js r128	WebGL を簡単に扱うための 3D ライブラリ
HTML / JavaScript	シンプルな構成で動作
📚 カスタマイズ例
色を変更する

ワイヤーフレームをオフにする

ライトを追加して質感を出す

複数オブジェクトを配置する

カメラ操作（OrbitControls）を追加する
