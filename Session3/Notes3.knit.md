---
title: "Notes3"
author: "Haoran Xu"
date: "2024-09-20"
output: html_document
---



## 笔记

可以不用特别注重格式，但是要注重自己的writing
The importance of **a good filing system** <- computers are filing machines (e.g., duo : linux and Windows)
working directory

pathway的问题：
e.g., 文件的pathways不能是只能compatible自己电脑文件的形式
解决方式：

## project

比较好的filing system示例:
README.md, bibliography, data, figures, paper, editorial correspondence, WGIT (e.g., a conference name)

Quarto 主要特点：
- 多语言支持：不仅支持 R，还支持 Python、Julia 和 Observable JavaScript。
- 灵活的输出格式：支持导出到多个格式（HTML、PDF、Word 等），可以用来生成静态或动态内容。
- 集成性：与 RStudio 无缝集成，可以直接在 RStudio 中创建和编写 Quarto 文档。
- 扩展性：可以使用插件、定制样式和模板进行扩展。

Quarto 文件的后缀是 .qmd，它类似于 .Rmd 文件，但提供更多的功能和选项。




``` r
# which(usethis) #  查询是否有这个包
# install.packages(usethis) # 下载这个包

# ?usethis
# library(usethis)  # 每次都需要用library()索引
# ?usethis

# usethis::create_project()  #其实可以省略成下面的样子，但是用"packages::"这样的形式会更加明确
# create_project()
```

project中的assests(shp, spreadsheet, images, other programming studd: matlab/python folder
data folder里面也可以分不同的folder: 比如geodata里面专门放shp data)
ps: 如果要考虑多张图片的排版，不要直接用r来写空格之类的，可以尝试用一些其他的approach ()

这个project里面的".rproj"文件打开之后只是console的东西，并没有实质的rmd内容


## 路径的选择

### 关于absolute/relative path

Example of an absolute path:
C:\Antonio\Courses\Reproducible-Research-Workflow\Session-03-Projects-and-Reproducible-Environments

Example of a relative path:
{here}\Session-03-Projects-and-Reproducible-Environments


``` r
# install.packages("here")
# install.packages("usethis")
# install.packages("renv")
```

I am doing an experiment in citing an image path [(here)](https://here.r-lib.org/). # use hyperlink

This is an image

![](Hiking on Cootes Paradise - Sep 10.jpg)  # 需要把rmd文件和imag文件放在同一个包里


## reproducible environments

reproducible environments provide functionality to *isolate package libraries and to make them portable.*

create a file that tell you what is in "library" environment

`renv::init()` 可以用来查看所有的packages

这个“renv.lock”文件展示了所有的packages

`renv::install()`会自动进入lock file, 会认为你的project需要这个package







