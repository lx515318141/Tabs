# 1.组件全局引用
    若组件个别页面引用，可以进行局部引用；若组件在大多数页面都需引用，则需要进行全局引用。
    创建组件文件夹，在其中创建组件文件及index.js文件，在index.js中引入组件：
    import Hello from "./Hello"
    export default (Vue) => {
        Vue.component(Hello.name,Hello)
    }
    再在main.js中引入：
    import Hello from './components/Hello'
    Vue.use(Hello)
    最后在需要使用的页面的template中直接使用 <Hello /> 即可。
# 2.tabs
    