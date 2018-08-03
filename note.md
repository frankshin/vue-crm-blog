from: https://vuejs-templates.github.io/webpack/structure.html

├── build/                     # webpack config files
│   └── ...
├── config/
│   ├── index.js               # main project config
│   └── ...
├── src/
│   ├── main.js                # app entry file
│   ├── App.vue                # main app component
│   ├── components             # ui components
│   │   └── ...
│   └── assets                 # module assets (processed by webpack)
|   └── strore
|       ├── index.js           # 我们组装模块并导出 store 的地方
|       ├── actions.js         # 根级别的 action
|       ├── mutations.js       # 根级别的 mutation
|       └── modules
|           ├── cart.js        # 购物车模块
|           └── products.js    # 产品模块
├── static/                    # pure static assets (directly copied)
├── test/
│   └── unit/                   # unit tests
│   │   ├── specs/              # test spec files
│   │   ├── eslintrc            # config file for eslint with extra settings only for unit tests
│   │   ├── index.js            # test build entry file
│   │   ├── jest.conf.js        # Config file when using Jest for unit tests
│   │   └── karma.conf.js       # test runner config file when using Karma for unit tests
│   │   ├── setup.js            # file that runs before Jest runs your unit tests
│   └── e2e/                    # e2e tests
│   │   ├── specs/              # test spec files
│   │   ├── custom-assertions/  # custom assertions for e2e tests
│   │   ├── runner.js           # test runner script
│   │   └── nightwatch.conf.js  # test runner config file
├── .babelrc                    # babel config
├── .editorconfig               # indentation, spaces/tabs and similar settings for your editor
├── .eslintrc.js                # eslint config
├── .eslintignore               # eslint ignore rules
├── .gitignore                  # sensible defaults for gitignore
├── .postcssrc.js               # postcss config
├── index.html                  # index.html template
├── package.json                # build scripts and dependencies
└── README.md

build/：
此目录包含开发服务器和生产webpack构建的实际配置。 通常，除非要自定义Webpack加载器，否则不需要触摸这些文件，在这种情况下，您应该查看build / webpack.base.conf.js。

config/index.js:
这是主要配置文件，它公开了构建设置的一些最常见的配置选项。 有关详细信息，请参阅开发期间的[API代理](https://vuejs-templates.github.io/webpack/proxy.html)和与[后端框架集成](https://vuejs-templates.github.io/webpack/backend.html)。

/src:
这是您的大多数应用程序代码所在的位置。如何构建此目录中的所有内容在很大程度上取决于您; 如果您使用的是Vuex，则可以参考Vuex应用程序的建议。

/static:
此目录是您不希望使用Webpack处理的静态资产的转义窗口。 它们将直接复制到生成webpack构建资产的同一目录中。
有关详细信息，请参阅[处理静态资产](https://vuejs-templates.github.io/webpack/static.html)

/test/util:
包含单元测试文件，详见[单元测试](https://vuejs-templates.github.io/webpack/unit.html)

/test/e2e:
包含e2e测试相关文件。 有关更多详细信息，请参阅[端到端测试](https://vuejs-templates.github.io/webpack/e2e.html)。

index.html
这是我们单页面应用程序的模板index.html。 在开发和构建期间，Webpack将生成资产，这些生成的资产的URL将自动注入此模板以呈现最终的HTML。

package.json
包含所有构建依赖项和[构建命令](https://vuejs-templates.github.io/webpack/commands.html)的NPM包元文件。

store:
详见项目结构：https://vuex.vuejs.org/zh/guide/structure.html