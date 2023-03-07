### 用例名称
创建工作空间

### 简要说明
开发者在平台中创建属于自己的工作空间。

### 优先级
高

### 前置条件
用户登录

### 后置条件
开发者创建工作空间生成任务，等待任务结束。任务中不可操作，任务成功允许对工作空间管理，任务失败，提示并点击重试或删除

### 事件流

#### 基流
  1. 普通开发者，进入**工作空间**页面，点击**创建**按钮，页面跳转进入创建工作页面
  2. 普通开发者在**创建工作空间**页面，展示四种TAB选项类别的模板，包含“系统内置模板”，“个人模板”，“团队（组织）模板”，
  开发者点击TAB选择切换，切换页面展示相应类别的模板列表，页面默认显示为“系统内置模板”，并展示系统内置模板列表内容
  3. 开发者在相应的TAB页下，通过输入**关键字**，点击**查询**按钮后查询到符合条件的模板
  4. 开发者选择**模板**，显示勾选
  5. 开发者点击**运行配置**项，弹出列表，"4核8G内存"、"4核16G内存"等，选中配置项
  6. 开发者点击页面最下方的**确定**按钮，页面跳转回**工作空间**列表
  7. 开发者在**工作空间**列表查询创建进度状态

#### 分支流
  - 2.1. 开发者通过"个人模板"TAB页面，如果符合条件选择模板  
  - 2.2. 如果没有满足开发者要求，开发者点击**自定义创建**，页面跳转到**个人模板自定义创建**页面，创建成功后开发者回到**基流**`1`、`2`，**分支流**`2.1`

#### 替代流
无
### 非功能需求
  1. 创建任务耗时，需要异步处理，但最大耗时应不超过60s

### 扩展点
