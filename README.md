# ionic-vue-kickstart
Kickstart project for cross-platform app development using ionic framework and vue.js

## Start

```
npm install -g @ionic/cli
ionic start develad-app blank --type vue
cd develad-app
ionic serve
```

### Documentation
- [Ionic Vue: Overview](https://ionicframework.com/docs/vue/overview)
- [Ionic Vue: Quick Start](https://ionicframework.com/docs/vue/quickstart)
- [Ionic Vue: Build First App](https://ionicframework.com/docs/vue/your-first-app)

## Deployment
```
ionic build
ionic cap add ios
ionic cap add android

ionic cap copy
ionic cap sync
```

### Documentation
- [Ionic Vue: Deploying](https://ionicframework.com/docs/vue/your-first-app/deploying-mobile)