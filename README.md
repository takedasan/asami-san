# asami-san
Oculus Quest版のVRChatで自分が使う用のモデルです。  
![VRChat](https://user-images.githubusercontent.com/33456217/57140553-fb787700-6df2-11e9-8f2a-c8343829e165.png)  

## 内容物
* image配下
元の三面図  
* asami-san.blend
モデルファイル  
* 各種PNG
テクスチャファイル  

### モデル
* Humanoidリグとウェイト設定
* 各種リップシンクシェイプキー
* 瞬きシェイプキー

## ライセンス
MITライセンスです。  
ライセンスの範囲でご自由にご利用ください。  

## おまけ:VRChat用のUnity設定方法
Unity2017 4.15f1での設定方法です。  
このリポジトリをCloneしてある前提です。  

1. FBXファイルのエクスポート  
BlenderからエクスポートでFBXファイルをエクスポート。  
ライトをエクスポート対象から外して後は全部エクスポートします。  
(あとで、Unity上でも削除できるのでめんどくさかったらやらなくてもOK)  

1. アセットの読み込み  
`Import New Assets`でFBXファイルと各種テクスチャPNGファイルをインポート。  

1. テクスチャのShader設定  
FBXファイルを選択して、MaterialsからLocationを`Use External Materials`に変える。  
![image](https://user-images.githubusercontent.com/33456217/57137756-c7e61e80-6deb-11e9-9c41-0af334179295.png)  
FBXファイルを展開してbody/hair/head/kara/wappenのShaderを`Unlit/Texture`に変える。  
![image](https://user-images.githubusercontent.com/33456217/57137902-29a68880-6dec-11e9-885b-2540e17162ae.png)  

1. Rigの設定  
FBXファイルを選択して、RigからAnimation Typeを`Humanoid`に変えて、Applyを押す。  
![image](https://user-images.githubusercontent.com/33456217/57138021-886c0200-6dec-11e9-8cfd-cf67c5c1da95.png)
Configure...ボタンを押して、設定を確認する。  
`Chest`だけ自動設定されてないので、手動で設定する。  
![image](https://user-images.githubusercontent.com/33456217/57138171-f4e70100-6dec-11e9-814a-b1680ff04378.png)  

1. Sceneに配置  
SceneにFBXファイルを配置。  
Transformを画像の通りに設定。  
(Scaleはお好みで。画像の通りだとモデルが160cmなので、縮小されて140cmになります)  
![image](https://user-images.githubusercontent.com/33456217/57138423-98381600-6ded-11e9-8849-4bcbf40f9728.png)  

1. VRChat設定  
Add ComponentボタンからScripts -> VRCSDK2 ->VRC_Avator Descripterでスクリプトを付与します。  
画像の通り設定。  
(View Positionはモデルの身長に応じてお好みで設定してください)  
![image](https://user-images.githubusercontent.com/33456217/57138573-fcf37080-6ded-11e9-8778-df1f791d9d91.png)  

1. 瞬き設定  
ここを参考にAnimatorを設定。  
https://jellyfish-qrage.hatenablog.com/entry/2018/10/02/152316

1. アップロード  
書かずとも、沢山記事があると思うので割愛。  