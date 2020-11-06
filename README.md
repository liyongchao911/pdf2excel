English version, Chinese see below:
## pdf Measurment Report to excel
### 0. This Project focus on 2 points:
 1. collect useful information in pdf measurment report(usually in pdf file), and statistic them to excel or csv with Pandas
 2. find the a way to automaticly process a batch of this files, for examlpe: 10000 files

### 1. This is a project for extract the measurement items and values from measurement report automaticly.

  - measurement report: usually a pdf file which record the measuremnt values from the samples
    which used for measuring.
  - measurement item: for the physical part, there are several features need to be controled
    during generate process(like plastic mold, steel stamping, machining, casting etc). For controling
    Sample the part from procsss and measure the key features, such as diameter, run-out, roughness etc.
    This key features are show as measurement item in the report
  - measurement value: measurement item values, often measuremet by CMM, scale..etc

### 2. Project scope

  - This project focus on get the measurement items and values from measurment report
  - Manually collect the needed values from a batch of pdf reports files often needs lots of time, and eadily get mistake.
  - This project will introduce a Python 3rd module, pdfplumber to convert the pdf file to text
  - Extract the needed information for text, and write it to Pandas DataFrame or to a excel/csv file

### 3. Project pipeline
  - 1. open to pdf file with pdfplumber to a pdfplumber object
  - 2. extract tables/text from the 1st step object
  - 3. extract needed information from tables/text
  - 4. write 3rd step information to a DataFrame
  - 5. For a batch process task, re-do step1 to step 4

Why DataFrame ?
if a data visuallilization and analysis is required, can use the Pandas and matplotlib do such
activities based on Pandas Dataframe API

### 4. More steps/Future work
  - Current code can only parse all the item in the pdf report, one more step need to add a function that make the customer input the item they inserset
  - Add a interface to relize the above function
  - Package this functioin to exe, then it can run without the development environment
  
### 5. Development platform:
  - 1. windows 10
  - 2. Anaconda + Jupyter notebook
  - 3. Python 3.8.3
-----------------------------------------------------------------

本项目涉及到工业生产中，批量从pdf测量报告中提取需要信息的一般化操作
## 批量提取pdf测量报告中测量值，并统计整理/写入excel/csv文件
### 0. 该项目涉及两个问题点:
 1. 使用pdfplumber、pandas库从pdf格式的测量报告中提取需要的测量值，可以加入可视化功能
 2. 多份文档的批量处理功能。可以一次性批量处理多份同类型的报告，经测试1000报告可以在5分钟之类处理完毕

### 1. 本项目可以完成从pdf测量报告中提取需要信息的功能.

 - 测量报告： 通常为一个pdf文档，用来记录从被测量零件中通过测量设备获得的测量值的集合
 - 测量要素： 在一个零件实体中，通过监控一些重要特征值的表现来监控其加工过程（如注塑，冲压等）的稳定性。这些值包括直径，跳动，表面粗糙度等。
   这些特性即测量要素。测量报告中一般需要包含这些测量要素
 - 测量值： 通过测量设备（坐标仪、卡尺、CT等）获取到的测量要素的结果


### 2. 项目边界

  - 该项目用于从pdf测量报告文档中批量提取关注的测量要素的值
  - 通过第三方模块pdfplumber实现pdf到text的转换，或者提取pdf文档中的表格
  - 从text文档中批量提取测量值，并写入pandas构建的DataFrame

### 3. 数据处理流水线
  - 1. 通过 pdfplumber 打开pdf文档，并创建一个pdfplumber对象
  - 2. 从第1步中创建的对象中提取表格或者需要的text信息
  - 3. 从第2步的表格、文本中提取需要的信息
  - 4. 将第3步的信息写入DataFrame
  - 5. 重复1-4步，实现批量处理

为何使用Dataframe来记录数据？
在上面的场景中，通常需要展示所收集到的数据的趋势，例如产品加工表面粗糙度随批次的变化，
以此来作为依据，判断设备是否需要停机维护等。
使用DataFrame可以很方便的调用内部的plot方法查看，也可以方便的写入csv文档进行后期存档等。

### 4. 未来进一步完善
 - 1. 暂时只可以实现从测量报告解析处全部测量要素，不符合客户导向
 - 2. 增加一个客户输入截面，客户输入想要提取的测量测量，之后程序自动解析出感兴趣的部分
 - 3. 暂时程序只可以在开发环境中运行，需要打包成exe文件，脱离开发环境运行
 
### 5. 代码测试平台:
  - 1. windows 10
  - 2. Anaconda + Jupyter notebook
  - 3. Python 3.8.3
