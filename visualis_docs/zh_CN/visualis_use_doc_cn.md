> 使用文档
## 1. 基本使用文档
&nbsp;&nbsp;&nbsp;&nbsp;Visualis是基于Davinci进行开发的数据化BI产品，其支持原有的[Davinci用户用法](https://edp963.github.io/davinci/)，在此基础上，Visualis提供了更多额外的的功能点。主要为，结果集可视化、工作流使用、邮件使用。

## 2. 结果集可视化
&nbsp;&nbsp;&nbsp;&nbsp;Visualis支持对接DSS的交互式脚本分析，在脚本运行完成后，可以对脚本的结果集进行可视化分析，并且结果集会自动绑定到一个默认的Widget，支持简单的拖拽就能实现Widget的开发。
![scriptis visualis](./../images/visualis_scriptis_visualis.gif)

## 3. 工作流使用
&nbsp;&nbsp;&nbsp;&nbsp;Visualis对接了DSS工作流，在DSS侧创建工程时，会同步创建Visualis工程，在工作流中，拖拽Visualis节点，同步也会在该工程中创建对应的组件，在工作流中使用Widget时，Widget需要绑定一个上游表作为数据源，来开发可视化图形，相关实现原理可以参考[Widget节点绑定DSS结果集节点](./Visualis_sql_databind_cn.md)，通过拖拽Widget和Display，Dashboard三个组件，连接成线，即可实现一个可视化报表。
![visualis workflow](./../images/visualis_workflow.gif)  
&nbsp;&nbsp;&nbsp;&nbsp;目前Visualis1.0.0对接DSS1.1.0中新增了View节点，和Sql节点类似，但在和Widget节点联合使用时，选用非绑定，双击进入Widget中后，在View选择栏中进行选择保存。

## 4. 邮件使用
&nbsp;&nbsp;&nbsp;&nbsp;DSS提供数据输出节点，在部署安装DSS时，需要配置相关的邮件服务器配置，使用邮件前，需确保邮件服务器的可用性，在工作流中通过拖拽邮件节点，连线并依赖可视化节点，配置相关邮件选项，即可发送邮件，邮件发送的最终效果，可以通过Display和Dashboard的预览接口进行查看。
![sendemail](./../images/dss_sendemail.gif)

有些使用上的注意点，可以参考[Visualis接入DSS/Linkis注意点](./Visualis_dss_integration_cn.md)。
