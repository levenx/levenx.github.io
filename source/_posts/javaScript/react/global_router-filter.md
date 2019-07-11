---
title: 【react】全局路由统一拦截处理
date: 2019-07-08 13:15:44
photos: https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1562146098475&di=d38f5a0643942cf3746caba44c106c4d&imgtype=0&src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201801%2F16%2F20180116155559_eQPGR.thumb.700_0.jpeg
categories:
- 设计模式
tags:
- 设计模式
- 代理模式
---

### 代理模式

---
router.js
<pre><code>
import Home from '../pages/home'
import Article from '../pages/article'

import User from '../pages/user'
import Role from '../pages/role'

const routers = [
  {
      title: '首页',
      path: '/',
      icon: 'icon-iconset0123',
      component: Home
  },
  {
      title: '笔记',
      path: '/article',
      icon: 'icon-iconset0123',
      component: Article

  },
  {
      title: '权限管理',
      path: '/auth',
      icon: 'icon-lishihistory2',
      children: [
          {
              title: '用户',
              path: '/auth/user',
              icon: 'icon-icon-',
              component: User
          },
          {
              title: '角色',
              path: '/auth/role',
              icon: 'icon-navicon-jsgl',
              component: Role
          }
      ]
  }
];
export default routers;
</code></pre>

router.js
<pre><code>
class LvxRouter extends React.Component {

  render(){
      return (
          <HashRouter>
              <App>
                  <Switch>
                      <Route path="/login" component={Login}/>
                      <Route path="/" render={()=>
                          <Admin>
                              <Switch>
                                  {
                                      Routers.map((item, index)=>{
                                          return <Route key={index} path={item.path} exact
                                          render={props=> (true ? <item.component {...props}/> :
                                              <Redirect  to={{
                                                  pathname:"/login",
                                                  // state: {from: props.location}
                                              }}/>
                                              )}/>
                                      })
                                  }
                                  {/* <Route component={Login}/> */}
                              </Switch>
                          </Admin>
                      }/>
                      <Route component={Login}/>
                  </Switch>
              </App>
          </HashRouter>
      );
  }

}
export default LvxRouter;
</code></pre>
