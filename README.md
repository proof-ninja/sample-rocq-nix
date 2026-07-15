# sample-rocq-nix

[![CI](https://github.com/proof-ninja/sample-rocq-nix/actions/workflows/ci.yml/badge.svg)](https://om/proof-ninja/sample-rocq-nix/actions/workflows/ci.yml)

Rocq プロジェクトを Nix と GitHub Actions でビルドする最小構成のサンプルです。

特徴:

- Rocq を opam でインストールしない
- GitHub Actions で Nix のバイナリキャッシュを利用
- `rocq makefile -f _RocqProject` で Makefile を生成
- 生成された Makefile を使ってビルド

## ファイル構成

```tree
.
├── _RocqProject
├── theories/Main.v
├── flake.nix
├── .github/
│   └── workflows/
│       └── ci.yml
└── README.md
```
## ローカルビルド

```
nix develop
```
```
rocq makefile -f _RocqProject -o Makefile
make
```
