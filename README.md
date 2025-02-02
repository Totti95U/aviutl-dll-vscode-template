## 概要
Visual Studio Code (vscode) 上で `.dll` ファイルを使用する AviUtl スクリプトを作るためのひな形です。
フォルダをコピーすることで、すぐに使える状態になります。

## 準備
事前準備として以下が必要です
- C/C++ コンパイラ (このプロジェクトの作成時は (i686-14.2.0-release-win32-dwarf-msvcrt-rt_v12-rev1)[https://github.com/niXman/mingw-builds-binaries/releases/tag/14.2.0-rt_v12-rev1] を使用しました)
    - 32bit 版のコンパイラを使用してください (AviUtl が 32bit アプリケーションのため)
    - このプロジェクトのコンフィグをそのまま使用したい場合は、用意した MinGW-W64 のパスを `PATH` に追加し、`g++ --version` でコンパイラのバージョンが表示されることを確認してください
- vscode の拡張機能のインストール
    - C/C++ Extension Pack
    - Code Runner

## 使い方
基本的な使い方は以下の通り
0. このフォルダをコピーする
1. `src` フォルダにある `main.cpp` を編集する
2. `main.cpp` をビルドする (デフォルトショートカット: `Ctrl + Shift + B`)
3. `build` フォルダに `main.dll` が生成される
4. `test.anm` を編集する
5. AviUtl の `script` フォルダに作成した `.dll` ファイルと `.anm` ファイルを置く
6. AviUtl を起動し、アニメーション効果から作成したスクリプトを読み込む

## リンク集
- [AviUtl](http://spring-fragrance.mints.ne.jp/aviutl/)
- [Visual Studio Code - Code Editing. Redefined](https://code.visualstudio.com)
- [GitHub - niXman/mingw-builds-binaries: MinGW-W64 compiler binaries](https://github.com/niXman/mingw-builds-binaries)
- [LuaBinaries - Browse /5.1.4/Windows Libraries at SourceForge.net](https://sourceforge.net/projects/luabinaries/files/5.1.4/Windows%20Libraries/)
    - `lua5_1_4_Win32_dll8_lib.zip` を使用してください (バージョンを上げるとエラーがでます)
- [AviUtlのスクリプト用にDLLつくろう #C++ - Qiita](https://qiita.com/SEED264/items/b57927e1dadb044cf614#%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%97%E3%83%88%E5%81%B4%E3%81%AE%E5%87%A6%E7%90%86)
- [備忘録　AviUtlでDLLスクリプトを書く方法 #C++ - Qiita](https://qiita.com/shulmj_/items/1a8e146887b825a77785)