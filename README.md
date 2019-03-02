# subtitleHelper
此脚本基于PHP  
目的是完善基于网易见外工作台的视频字幕自动化流程  
适用于见外工作台+PR流程  
# 原流程及问题分析
1. 使用PR剪辑视频  
2. 提取音频  
3. 上传音频并使用网易见外工作台的语音转写功能（选择输出格式为字幕SRT）  
4. 导出并导入PR工程  
  
问题在于第四步骤  
导出的SRT文件时间轴重合  
上一句字幕的结束时间与下一句字幕的开始时间一致  
PR无法识别此种字幕SRT  
此脚本对导出的SRT文件进行处理  
自动生成PR可完美识别的SRT字幕  
# 如何使用此脚本
1. 搭建PHP环境及localhost
2. 将见外工作台导出的SRT文件拖入目录
3. 更改file_get_contents()中的参数为SRT文件的目录名称
4. 在目录自动生成名为new_test.srt的SRT文件