# rust-vscode-devcontainer-for-atcoder

これはRustでAtCoderのコンテストに参加する為のVS Code のDevContainerのリポジトリです。  
このリポジトリをVS CodeのDevContainerで開く事で、以下の事が出来るようになります。  
- rust-analyzerによるコード補完
- ファイル保存時にrustfmtによるコード整形
- [cargo-atcoder](https://crates.io/crates/cargo-atcoder)によるテストケース実行やサブミット
また、GitHub Codespacesを利用する事で、ブラウザ版のVS Codeで同じ環境を使う事が出来ます。  
VS Codeの設定を自分好みに変更したい場合は、```rust-vscode-devcontainer-for-atcoder/.devcontainer/devcontainer.json```の"settings"や"extensions"を変更したリポジトリを使って下さい。  
cargo-atcoderの設定```rust-vscode-devcontainer-for-atcoder/cargo-atcoder.toml```を変更したリポジトリを使って下さい。  

## コンテナ環境での主な使い方

コンテナ環境に入ったら、VS Code内のターミナルで以下のようにコンテスト用のプロジェクトを作成し、作成したフォルダに移動します。  
```
cargo atcoder new abc283
cd abc283
```
サブミットするにはAtCoderへのログインが必要です。VS Code内のターミナルで以下のコマンドを実行します。  
```
cargo atcoder login
```
まずa問題を特には、src/bin/a.rs を編集し、サンプルでのテストを行います。VS Code内のターミナルで以下のコマンドを実行します。  
```
cargo atcoder test a
```
提出するには、VS Code内のターミナルで以下のコマンドを実行します。  
```
cargo atcoder submit a
```
詳しくは[cargo-atcoder](https://crates.io/crates/cargo-atcoder)を参照して下さい。  

## LICENSE

Apache-2.0
