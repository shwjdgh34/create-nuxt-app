# nuxt-app

> create-nuxt-app

## Build Setup

```bash
# install dependencies
yarn install

# serve with hot reload at localhost:3000
yarn dev

# build for production and launch server
yarn build
yarn start

# generate static project
yarn generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).

## Tip for nuxt

### router

#### 1. anchor tag

```html
<a href="/users">Users</a>
```

'User' page is loded by sending a new request to the server and rendering back a new page. this is server side rendering. When you wanna stick to the new single page application that still runs because remember what i said in the first module, dont use this. By using this, we're always getting a new page.

#### 2. nuxt-router

```html
<nuxt-link to="/users">Users</nuxt-link>
```

Once the first page is pre-rendered we still have a single page application because we want to stay in that fast and instant responses. nuxt-router makes us use single pages application but it is a bit different with normal one. The main difference to a normal spa is that all starting pages for different url can be pre-rendered entirely on the server instead of in the client

This is 'universal' which is SPA + SRR

> [ssr-spa-nuxt](https://medium.com/aha-official/%EC%95%84%ED%95%98-%ED%94%84%EB%A1%A0%ED%8A%B8-%EA%B0%9C%EB%B0%9C%EA%B8%B0-1-spa%EC%99%80-ssr%EC%9D%98-%EC%9E%A5%EB%8B%A8%EC%A0%90-%EA%B7%B8%EB%A6%AC%EA%B3%A0-nuxt-js-cafdc3ac2053)

### layout

#### 1. style

default.vue 의 style을 default로 하고 users.vue 에 추가적으로 있는 style만 덮어씌운다.

#### 2. usage

사용하고 싶은 layout을 script에 적는다.

```js
export default {
  layout: 'users'
}
```

> layout/users.vue 를 사용한 경우

layout을 명시하지 않으면 layout/default.vue가 default로 적용된다.

#### 3. inherit

if you applied layout to parent page, it would be inherited to nuxt-childs which are nested routes. This mean that you don't need to add layout on any page of childs
