# 前言

欢迎来到基于SSM的宿舍卫生评比系统项目。此项目致力于为高校宿舍管理人员提供一个便捷、高效的卫生评比解决方案。通过此系统，可以实时监控宿舍卫生状况，提高学生宿舍卫生意识。

## 内容介绍

本项目主要包括以下功能：宿舍卫生评分、卫生排名、评分记录查询、宿舍信息管理、用户权限管理等。系统采用前后端分离的开发模式，前端负责展示与交互，后端负责数据处理与存储。通过使用Spring、SpringMVC和MyBatis等框架，实现了高内聚、低耦合的代码结构，便于后期维护与扩展。

## 技术介绍

### 语言：Java
### 使用框架：Spring、SpringMVC，MyBatis
### 前端技术：JS、Vue、CSS3
### 开发工具：IDEA/Eclipse
### 数据库：MySQL 5.7/8.0
### 数据库管理工具：phpstudy/Navicat
### JDK版本：jdk1.8
### Maven: apache-maven 3.8.1-bin
### 前端环境：Node.Js 12\14\16

## 核心代码

以下是本项目中的部分核心代码，实现了宿舍卫生评分的功能：

```java
// 宿舍卫生评分接口
@RestController
@RequestMapping("/api/healthScore")
public class HealthScoreController {

    @Autowired
    private HealthScoreService healthScoreService;

    // 新增评分记录
    @PostMapping("/add")
    public Result addHealthScore(@RequestBody HealthScore healthScore) {
        // 校验参数
        if (Objects.isNull(healthScore) || healthScore.getScore() <= 0) {
            return Result.error("参数错误");
        }
        // 新增评分记录
        boolean flag = healthScoreService.addHealthScore(healthScore);
        return flag ? Result.success("添加成功") : Result.error("添加失败");
    }

    // 查询评分记录
    @GetMapping("/list")
    public Result listHealthScores(@RequestParam("dormitoryId") int dormitoryId,
                                   @RequestParam("date") String date) {
        // 查询评分记录
        List<HealthScore> healthScores = healthScoreService.listHealthScores(dormitoryId, date);
        return Result.success(healthScores);
    }
}
```

## 免费源码获取

```
5000套系统成品在线演示视频，复制到流浪器： 
```
```
https://www.yuque.com/yuqueyonghux32e1j/kxdc9g/ad8oz3bamkxmay0e#Cxun
```
![下载](https://img12.360buyimg.com/ddimg/jfs/t1/339687/11/1349/28408/68ad865fF412d7877/adaa650483a100f2.jpg)

## 项目截图

![封面图片](https://img11.360buyimg.com/ddimg/jfs/t1/333281/28/11882/136536/68c1b389Fe46ef160/eb235d659bc3d5c6.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/348641/24/1739/69254/68c1b361F7290ddc0/616a9b598c77ae07.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/344733/28/1882/23190/68c1b361F9227d1a6/026df703162c619e.jpg)

![介绍图片](https://img12.360buyimg.com/ddimg/jfs/t1/343365/5/1975/44084/68c1b362Fa3f7c962/4cc40b6ea7b0619a.jpg)

![介绍图片](https://img11.360buyimg.com/ddimg/jfs/t1/324448/36/18763/59184/68c1b362F5aa92432/f6594305a07752f3.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/327522/25/18483/24574/68c1b362F14611c2b/5bcfa8115b34804d.jpg)

![介绍图片](https://img11.360buyimg.com/ddimg/jfs/t1/326672/39/18700/46295/68c1b362Ff14713c7/0f9588df6cbb1744.jpg)

![介绍图片](https://img14.360buyimg.com/ddimg/jfs/t1/329991/3/11428/21953/68c1b362F12b48faa/746bbb9c23ddd9ab.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/323258/17/12891/25443/68c1b362F1e4cf2a7/39333ee1ee2ddf73.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/325749/2/18768/18747/68c1b363Fded1d4e8/a497a36fa7373278.jpg)
