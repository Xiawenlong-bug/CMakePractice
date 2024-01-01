#设置项目名称 HELLO
PROJECT (HELLO)
#PROJECT(projectname [CXX] [C] [Java])
#你可以用这个指令定义工程名称，并可指定工程支持的语言，支持的语言列表是可以忽略的，
#默认情况表示支持所有语言。这个指令隐式的定义了两个cmake 变量:
#<projectname>_BINARY_DIR 以及<projectname>_SOURCE_DIR


#变量SRC_LIST 赋值 main.c
SET(SRC_LIST main.c)

#MESSAGE 输出log 
#SEND_ERROR，产生错误，生成过程被跳过
#SATUS，输出前缀为—的信息
#FATAL_ERROR，立即终止所有 cmake 过程
#${}取出变量值
MESSAGE(STATUS "This is BINARY dir " ${HELLO_BINARY_DIR}) 


#隐式变量 HELLO_SOURCE_DIR 即  <项目名称>_SOURCE_DIR
MESSAGE(STATUS "This is SOURCE dir " ${HELLO_SOURCE_DIR}) 

#ADD_EXECUTABLE 生产执行文件
ADD_EXECUTABLE(hello ${SRC_LIST})
