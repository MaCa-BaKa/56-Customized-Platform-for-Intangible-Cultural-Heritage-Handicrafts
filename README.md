# 56-非遗手工艺品定制平台系统

[文档地址](http://wechat.zjrcsy.cn/)

技术栈：Spring Boot 3 + Spring Security + JWT + Spring Data JPA + MySQL + Vue 3 + Vite + Pinia + Vue Router + Element Plus + Axios

## 补充说明

- 后端技术要点：Spring Boot、Spring Security、JWT 鉴权、Spring Data JPA、MySQL、统一响应封装、本地文件上传与访问、支付宝沙箱支付配置、用户/商家/管理员三端权限控制。
- 前端技术要点：Vue 3、Vite、Element Plus、Pinia、Vue Router、Axios，采用用户端、商家端、管理端三套布局与路由体系。


## 用户端

1. **登录入口：** 支持用户端、商家端、管理端分角色进入，用户登录后访问前台商城功能。
2. **首页：** 展示非遗主题轮播图、热门推荐商品、商品入口与文化资讯入口。
3. **非遗好物：** 支持商品列表浏览、分类筛选、关键词搜索、商品价格与库存展示。
4. **商品详情：** 展示商品图片、价格、评分、库存、地域标签、工艺详情、文化背景、商家信息；支持立即下单、加入购物车、收藏。
5. **商家店铺：** 用户可进入商家主页查看店铺介绍与该商家的商品。
6. **定制服务：** 支持按商品发起定制需求，提交文字需求、图片、收货信息并查看定制进度。
7. **购物车：** 按商家归类购物车商品，支持勾选结算、数量调整与订单创建。
8. **订单中心：** 查看普通订单与定制订单，跟踪支付、发货、收货、完成等状态。
9. **收藏中心：** 支持收藏商品或商家，便于后续复购与关注。
10. **在线咨询：** 用户可与商家沟通商品、订单和定制需求。
11. **个人中心：** 维护头像、昵称、联系方式、密码和收货地址。
12. **文化资讯：** 浏览非遗文化文章，了解技艺背景、工艺故事和传承知识。


## 商家端

1. **数据统计：** 汇总订单量、销售额、客单价、定制需求、热门商品与分类统计。
2. **商品管理：** 商家可新增、编辑、上下架商品，维护商品图片、价格、库存、分类、工艺详情与文化背景。
3. **订单管理：** 查看用户订单，按状态筛选并处理发货、完成等订单流程。
4. **定制管理：** 管理用户提交的定制需求，查看需求详情、图片和处理状态。
5. **在线咨询：** 与用户进行订单和定制相关沟通。
6. **个人中心：** 维护商家店铺资料、头像、联系方式和基础信息。


## 管理端

1. **数据统计：** 展示平台用户数、商家数、商品数、订单数、交易额、活跃与定制趋势、商品/商家/分类排行。
2. **用户管理：** 管理用户与商家账号，支持检索、分页、账号状态维护和基础资料查看。
3. **商家审核：** 审核商家资质，查看店铺信息并处理入驻申请。
4. **商品管理：** 审核商家发布的商品，维护商品上架状态并处理不合规商品。
5. **分类管理：** 管理非遗商品分类，支持父子分类、排序和增删改。
6. **轮播图管理：** 配置首页轮播图，维护图片、标题、排序和启用状态。
7. **文化资讯：** 发布、编辑与管理非遗文化文章。
8. **评价管理：** 查看商品评价，支持按评分或关键词筛选并处理异常评价。
9. **个人中心：** 管理平台管理员个人资料与登录信息。


## 用户端界面示意

![登录入口](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/01_login_entry.png)

![用户端首页](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/02_user_home.png)





![文化资讯](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/05_user_cultural.png)

![购物车](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/06_user_cart.png)

![我的订单](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/07_user_orders.png)


## 商家端界面示意

![商家数据统计](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/08_merchant_stats.png)

![商家商品管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/09_merchant_product.png)

![商家订单管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/10_merchant_order.png)

![商家定制管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/11_merchant_custom.png)


## 管理端界面示意

![管理端数据统计](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/12_admin_stats.png)

![用户管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/13_admin_user.png)

![商家审核](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/14_admin_merchant.png)

![商品管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/15_admin_product.png)

![分类管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/16_admin_category.png)

![轮播图管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/17_admin_carousel.png)

![文化资讯管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/18_admin_article.png)

![评价管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/19_admin_review.png)

