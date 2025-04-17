# tmux-tabicon-theme

[tmux-tabicon](https://github.com/mocaffy/tmux-tabicon) のテーマコレクションです。プロセス名に応じて自動的にアイコンを表示するための設定が含まれています。

## 含まれるテーマ

- `normal` - 基本的なアイコンセット
- その他のテーマは `themes` ディレクトリを参照してください

## 前提条件

- [TPM (Tmux Plugin Manager)](https://github.com/tmux-plugins/tpm) がインストールされていること
- [tmux-tabicon](https://github.com/mocaffy/tmux-tabicon) プラグインがインストールされていること

## インストール方法

1. TPMをインストール（まだの場合）:
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

2. このテーマリポジトリをクローン:
```bash
git clone https://github.com/mocaffy/tmux-tabicon-theme.git ~/.config/tmux/tabicon-theme/
```

3. tmux.confに以下を追加:
```tmux
# テーマディレクトリの設定
set -g @tmux-tabicon-themes-dir ~/.config/tmux/tabicon-theme/

# プラグインの設定
set -g @plugin 'mocaffy/tmux-tabicon'

# テーマの選択（オプション、デフォルトは'normal'）
set -g @tmux-tabicon-theme 'normal'

# TPMの初期化（これは設定の最後に記述）
run '~/.tmux/plugins/tpm/tpm'
```

4. 設定を反映:
   - tmuxを起動中の場合: プレフィックス + I (大文字のI) を押してプラグインをインストール
   - または、tmuxを再起動

## カスタマイズ

独自のテーマを作成する場合は、`themes` ディレクトリ内の既存のテーマを参考にしてください。
各テーマは以下の要素を含むことができます：

- プロセス名とアイコンのマッピング
- アイコンの色設定
- その他の表示形式のカスタマイズ

## ライセンス

このプロジェクトは[MITライセンス](LICENSE)の下で公開されています。
