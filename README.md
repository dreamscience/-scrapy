# -scrapy
猫眼电影scrapy爬取电影基本信息
目标网址（经典电影）：https://maoyan.com/films?showType=3&offset=0  30递增

数量：爬取67页 即offset=1980

所需信息：片名、猫眼评分，类型，时长，上映时间，导演，主演，剧情简介

工具：使用scrapy爬虫框架

猫眼评分和票房的数字编码对应表，猫眼口碑分数可以找到猫眼字体文件.eot,在http://fontstore.baidu.com/static/editor/index.html 百度字体编辑器查看对应字体编码
# 0-f489
# 1-e343
# 2-f19b
# 3-f848
# 4-e5e2
# 5-e8cd
# 6-f4ef
# 7-f88a
# 8-e137
# 9-e7a1
用xpath或正则提取，作比较得到评分数
maoyan_numbercode = ['f489','e343','f19b','f848','e5e2','e8cd','f4ef','f88a','e137','e7a1']
xpath出来的是 tuple元组类型数据，需要进一步处理
['\ue7a1.\ue8cd']
('e7a1', 'e8cd')

疯狂原始人 9.5
爵迹 7.8
一点就到家 9.2
鬼灭之刃 兄妹的羁绊 9.2
