English version, Chinese see below:
# pdf Measurment Report to excel
# 0. This Project focus on 2 points:
 1. collect useful information in pdf measurment report(usually pdf file), and statistic them to excel or csv with Pandas
 2. find the a way to automaticly process a batch of this file, for examlpe: 10000 files

#1. This is a project for extract the measurement item and value from measurement report automaticly.

  - measurement report: usually a pdf file which record the measuremnt values from the samples
    which used for measure
  - measurement item: for the physical part, there are several features need to be controled
    during generate process(like plastic mold, steel stamping, machining, casting etc). For controling
    Sample the part from procsss and measure the key features, such as diameter, run-out, roughness etc.
    This key features are show as measurement item in the report
  - measurement value: measurement item values, ofen measuremet by CMM, rules..etc

# 2. Project scope

  - This project focus on get the measurement item and values from measurment report
  - Collect all the pdf report values often manually need lots of time
  - This project will introduce a Python 3rd module, pdfplumber to convert the pdf file to text
  - Extract the needed information for text, and write it to Pandas DataFrame

# 3. Project pipeline
  - 1. open to pdf file with pdfplumber to a pdfplumber object
  - 2. extract tables/text from the 1st step object
  - 3. extract needed information from tables/text
  - 4. write 3rd step information to a DataFrame
  - 5. For a batch process task, re-do step1 to step 4

Why DataFrame ?
if a data visuallilization and analysis is required, can use the Pandas and matplotlib do such
activities based on Pandas Dataframe API

-----------------------------------------------------------------

本项目涉及到工业生产中，批量从pdf测量报告中提取需要信息的一般化操作
# 0. 该项目涉及两个问题点:
 1. 使用pdfplumber、pandas库从pdf格式的测量报告中提取需要的测量值，可以加入可视化功能
 2. 批量处理。加入测量报告有1000份，需要加入批量处理功能

#1. 本项目可以完成从pdf测量报告中提取需要信息的功能.

  - measurement report: usually a pdf file which record the measuremnt values from the samples
    which used for measure
  - measurement item: for the physical part, there are several features need to be controled
    during generate process(like plastic mold, steel stamping, machining, casting etc). For controling
    Sample the part from procsss and measure the key features, such as diameter, run-out, roughness etc.
    This key features are show as measurement item in the report
  - measurement value: measurement item values, ofen measuremet by CMM, rules..etc

# 2. Project scope

  - This project focus on get the measurement item and values from measurment report
  - Collect all the pdf report values often manually need lots of time
  - This project will introduce a Python 3rd module, pdfplumber to convert the pdf file to text
  - Extract the needed information for text, and write it to Pandas DataFrame

# 3. Project pipeline
  - 1. open to pdf file with pdfplumber to a pdfplumber object
  - 2. extract tables/text from the 1st step object
  - 3. extract needed information from tables/text
  - 4. write 3rd step information to a DataFrame
  - 5. For a batch process task, re-do step1 to step 4

Why DataFrame ?
if a data visuallilization and analysis is required, can use the Pandas and matplotlib do such
activities based on Pandas Dataframe API
