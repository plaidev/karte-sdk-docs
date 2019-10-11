# karte-sdk-docs

## Unity SDK APIリファレンスの更新方法

UnityのAPIリファレンスは[docfx](https://dotnet.github.io/docfx/)で生成しています。
リファレンスを更新するにはこのレポジトリのソースを直接修正せず、docfxでドキュメントを生成し直してください。
具体的な更新手順は以下の通りです。
1. [Unity SDK](https://github.com/plaidev/tracker-unity)をclone
1. Unity/Assets内のC#のソースコード中のコメントを編集
1. Unityディレクトリで `docfx docfx_project/docfx.json` を実行
1. Unity/docfx_projectに_siteディレクトリが生成されるのでそれをunityにリネームしてこのレポジトリのdocs/unityを上書き
