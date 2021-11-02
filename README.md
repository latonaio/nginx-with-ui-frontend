# nginx-with-ui-frontend  
nginx-with-ui-frontend は、主にエッジコンピューティング環境において、コンテナ化されたUIフロントエンドリソースとともにNGINXを立ち上げ、稼働させるためのリポジトリです。    
NGINXは、webサーバー、ロードバランサ、リバースプロキシ等の機能を有したオープンソースソフトウェアです。  
AION では、NGINXがコンテナ化された状態で軽量で高速に動作するため、UIフロントエンドリソースのコンテナ稼働環境基盤として、NGINXを利用しています。　　  

## Sample Dockerfile  
本レポジトリには、UIフロントエンドリソースとともにコンテナ稼働環境基盤としてNGINXを立ち上げ稼働させるための、サンプルの Dockerfile が含まれています。  

## UI Frontend リソース における NGINX の構築設定例    
たとえば、ui-frontend-for-omotebako において、次のように Dockerfile にて設定することによって、UIフロントエンドリソースのコンテナ稼働環境基盤として、UIフロントエンドリソースとともに NGINX を立ち上げ稼働させます。  

[ui-frontend-for-omotebako](https://github.com/latonaio/ui-frontend-for-omotebako)、Dockerfile 内      

```
CMD [ "nginx", "-g", "daemon off;" ]
```
