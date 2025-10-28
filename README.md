# matsushita_M1_any_genre_commentary
このリポジトリでは，各動画の実況音声の文字起こしのスクリプトが書かれたtxtファイルと，各動画の開始終了時刻をまとめたcsvファイルをを提供しています．

## Dataset structure / データセット構成
```
- csv/{ゲーム（スポーツ）の名前}_csv/各csvファイル
- txt/{ゲーム（スポーツ）の名前}_txt/各txtファイル
```

#### csvファイル: 
元の動画から，各試合を切り出すためのファイルです．
それぞれのファイルの名前は，{ゲーム（スポーツ）の名前}_{YoutubeのvideoID（11文字）}.csvとなっています．ex)Apex_3Qjog3M437Y.csv
YoutubeのvideoIDは，Youtubeの動画のリンク（ex)`https://www.youtube.com/watch?v=Zdam7_PgiT0`）のv=のあとに続く11文字を指します．
txtファイルのみ存在し，csvファイルが存在しない動画がありますが，その場合は，切り出しは行わずに，ダウンロードした動画をそのままデータセットとして使用しています．

| start   | end   | ID  |
| ---  | ---   | ---  | 
|4279    | 6014   |1   |
| ...       | ...   | ...   |

- `start`: 動画の中の各試合の開始時刻
- `end`: 動画の中の各試合の終了時刻
- `ID`: 動画の中で，その試合が何試合目に当たるかを記したID.1から順に割り当てられている．

#### txtファイル: 実況音声の文字起こしのスクリプト
各試合の実況の発話内容と，その発話の開始，終了時刻をまとめたファイルになります．
各要素はタブ区切りで保存されています．なお，それぞれのファイルの名前は，{ゲーム（スポーツ）の名前}_{YoutubeのvideoID（11文字）}.txtとなっています．ex)Apex_3Qjog3M437Y.txt
YoutubeのvideoIDは，Youtubeの動画のリンク（ex)`https://www.youtube.com/watch?v=Zdam7_PgiT0`）のv=のあとに続く11文字を指します．

| start_time  | end_time    | transcript  |
| --- | --- | --- |
| 298.52 | 299.52     | ついに手に入れた |  
| ... | ... | ... |

- `start_time`: 発話開始時刻．
- `end_time`: 発話終了時刻．
- `transcript`: 発話内容．



## License / ライセンス
- MIT

## Contributors / 貢献者
- Ryosuke Matsushita / 松下　嶺佑 (慶應義塾大学, main contributor)
- Shinnosuke Takamichi / 高道　慎之介 (慶應義塾大学，東京大学)

## Reference / 参考文献
- 
