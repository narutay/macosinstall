## MacOS のインストール
Xcode, Xcode Command-Line Tool のインストール
```bash
$ xcode-select --install
```

homebrewのインストール
```bash
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

ansible, gitのインストール
```bash
$ brew install ansible git
```

ansible実行前にApp Storeにログインをする

ansibleの実行
```bash
$ git clone https://github.com/narutay/osxinstall.git
$ cd macosinstall
$ vim macos_install.yml
# role: gitのユーザ名、emailを自分のものに書き換える
$ ansible-playbook -i hosts macos_install.yml -v
$ killall Finder
$ killall Dock
```

## その他、手動での作業
- FileVaultの有効化
- ファイアウォールの有効化
- ディスプレイ解像度の変更
- キーボードショートカットを`space` + `command`にする
- [システム環境設定] > [Siriの] のショートカットを無効にする
- 修飾キーの`Caps Lock`を`Control ^`に変更する
- BetterTouchToolの設定インポート(files/bettertouch_trigger.bttpreset