# cesium-on-vue

A demo app to use a Cesium Viewer within a Vue component

## Introduction

In my day job, we use Cesium to display 3D models. This is a proof of concept to demonstrate what's 
necessary to integrate Cesium within a Vue component.

## Reproducing this Project

1. First, I used the Vue CLI to create a new Vue project.
1. Second, I spent some time with Cesium's official [Webpack example](https://github.com/AnalyticalGraphicsInc/cesium-webpack-example).
1. I then integrated these build steps into `vue.config.js` so that vue could continue to drive the webpack build.
1. I followed recommendations from one of the raised [issues](https://github.com/AnalyticalGraphicsInc/cesium-webpack-example/issues/6) to squash Webpack warnings.
1. I created a Vue component with the stock Cesium viewer.
