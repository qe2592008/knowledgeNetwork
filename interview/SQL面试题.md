# SQL面试题
## 条件
四个表
### 学生表
Student(stuId,stuName,stuAge,stuSex) 
stuId：学号；stuName：学生姓名；stuAge：学生年龄；stuSex：学生性别
### 课程表
Course(courseId,courseName,teacherId) 
courseId,课程编号；courseName：课程名字；teacherId：教师编号
### 成绩表
Scores(stuId,courseId,score) 
stuId：学号；courseId,课程编号；score：成绩
### 教师表
Teacher(teacherId,teacherName) 
teacherId：教师编号； teacherName：教师名字
### 准备数据
insert into Student(stuId,stuName,stuAge,stuSex) values (1,'huahua',12,0);
insert into Student(stuId,stuName,stuAge,stuSex) values (2,'caocao',13,1);
insert into Student(stuId,stuName,stuAge,stuSex) values (3,'haohao',14,0);
insert into Student(stuId,stuName,stuAge,stuSex) values (4,'haha',15,1);
insert into Student(stuId,stuName,stuAge,stuSex) values (5,'wowo',16,0);
insert into Course(courseId,courseName,teacherId) values (1,'yuwen',1);
insert into Course(courseId,courseName,teacherId) values (2,'shuxue',2);
insert into Course(courseId,courseName,teacherId) values (3,'yingyu',3);
insert into Course(courseId,courseName,teacherId) values (4,'wuli',4);
insert into Course(courseId,courseName,teacherId) values (5,'huaxue',5);
insert into Teacher(teacherId,teacherName) values (1,'laoshi1');
insert into Teacher(teacherId,teacherName) values (2,'laoshi2');
insert into Teacher(teacherId,teacherName) values (3,'laoshi3');
insert into Teacher(teacherId,teacherName) values (4,'laoshi4');
insert into Teacher(teacherId,teacherName) values (5,'laoshi5');
insert into Scores(stuId,courseId,score) values (1,1,70);
insert into Scores(stuId,courseId,score) values (1,2,50);
insert into Scores(stuId,courseId,score) values (1,3,80);
insert into Scores(stuId,courseId,score) values (2,1,70);
insert into Scores(stuId,courseId,score) values (2,2,80);
insert into Scores(stuId,courseId,score) values (2,3,70);
insert into Scores(stuId,courseId,score) values (3,1,70);
insert into Scores(stuId,courseId,score) values (3,2,90);
insert into Scores(stuId,courseId,score) values (3,3,70);
insert into Scores(stuId,courseId,score) values (4,1,70);
insert into Scores(stuId,courseId,score) values (4,3,70);
insert into Scores(stuId,courseId,score) values (4,2,50);
insert into Scores(stuId,courseId,score) values (5,1,80);
insert into Scores(stuId,courseId,score) values (5,2,100);
insert into Scores(stuId,courseId,score) values (5,3,50);
insert into Scores(stuId,courseId,score) values (1,4,60);
insert into Scores(stuId,courseId,score) values (2,4,80);
insert into Scores(stuId,courseId,score) values (3,5,70);
insert into Scores(stuId,courseId,score) values (4,5,50);
## 题目
### 查询“001”课程比“002”课程成绩高的所有学生的学号
select stuId from Scores where 
(select score from Scires where courseId='001')
### 查询平均成绩大于60分的同学的学号和平均成绩
select stuId, avg(score) avgScore from Scores group by stuId having avgScore > 60;
#### 引申：获取满足以上条件的同学的信息
select * from Student where stuId in (select stuId from (select stuId, avg(score) avgScore from Scores group by stuId having avgScore > 60) as a);
select * from Student where stuId in (select a.stuId from (select stuId, avg(score) avgScore from Scores group by stuId having avgScore > 60) as a where a.stuId=stuId);
### 查询所有同学的学号、姓名、选课数、总成绩
select s.stuId,s.stuName,a.courseCount,a.totalScore from Student s,(select ss.stuId,count(1) as courseCount,sum(ss.score) as totalScore from Scores ss group by ss.stuId) as a where s.stuId=a.stuId;
select st.stuId,st.stuName,count(sc.courseId),sum(sc.score) from Student st left join Scores sc on sc.stuId=st.stuId group by sc.stuId;
### 查询姓“李”的老师的个数
select count(1) from Teacher where teacherName like '李%';
## 查询没学过“叶平”老师课的同学的学号、姓名
select st.stuId,st.stuName from Student st where st.stuId not in (select sc.stuId from Scores sc,Course co,Teacher t where sc.courseId=co.courseId and co.teacherId=t.teacherId and t.teacherName='laoshi1');

select sc.stuId from Scores sc,Course co,Teacher t where sc.courseId=co.courseId and co.teacherId=t.teacherId and t.teacherName='laoshi4';
select sc.stuId from Scores sc join Course co on sc.courseId=co.courseId join Teacher t on co.teacherId=t.teacherId where  t.teacherName='laoshi4';
### 查询学过“001”并且也学过编号“002”课程的同学的学号、姓名
select st.stuId,st.stuName from Student st,(select sc1.stuId from Scores sc1 where sc1.courseId='1') s1, (select sc2.stuId from Scores sc2 where sc2.courseId='4') s2 where s1.stuId=s2.stuId and s1.stuId=st.stuId;
### 查询学过“叶平”老师所教的所有课的同学的学号、姓名

### 查询课程编号“002”的成绩比课程编号“001”课程低的所有同学的学号、姓名

### 查询所有课程成绩小于60分的同学的学号、姓名

### 查询没有学全所有课的同学的学号、姓名

### 查询至少有一门课与学号为“1001”的同学所学相同的同学的学号和姓名

### 查询至少学过学号为“001”同学所有一门课的其他同学学号和姓名

### 把“Scores”表中“叶平”老师教的课的成绩都更改为此课程的平均成绩


### 查询和“1002”号的同学学习的课程完全相同的其他同学学号和姓名

### 删除学习“叶平”老师课的Scores表记录

### 向Scores表中插入一些记录，这些记录要求符合以下条件：没有上过编号“003”课程的同学学号、2、号课的平均成绩

### 按平均成绩从高到低显示所有学生的“数据库”、“企业管理”、“英语”三门的课程成绩，按如下形式显示： 学生ID,,数据库,企业管理,英语,有效课程数,有效平均分

### 查询各科成绩最高和最低的分：以如下形式显示：课程ID，最高分，最低分

### 按各科平均成绩从低到高和及格率的百分数从高到低顺序

### 查询如下课程平均成绩和及格率的百分数(用"1行"显示): 企业管理（001），马克思（002），OO&UML （003），数据库（004）

### 查询不同老师所教不同课程平均分从高到低显示

### 查询如下课程成绩第 3 名到第 6 名的学生成绩单：企业管理（001），马克思（002），UML （003），数据库（004）

### 统计列印各科成绩,各分数段人数:课程ID,课程名称,[100-85],[85-70],[70-60],[ <60]

### 查询学生平均成绩及其名次

### 查询各科成绩前三名的记录:(不考虑成绩并列情况)

### 查询每门课程被选修的学生数

### 查询出只选修了一门课程的全部学生的学号和姓名

### 查询男生、女生人数

### 查询姓“张”的学生名单

### 查询同名同性学生名单，并统计同名人数

### 1981年出生的学生名单(注：Student表中stuAge列的类型是datetime)

### 查询每门课程的平均成绩，结果按平均成绩升序排列，平均成绩相同时，按课程号降序排列

### 查询平均成绩大于85的所有学生的学号、姓名和平均成绩

### 查询课程名称为“数据库”，且分数低于60的学生姓名和分数

### 查询所有学生的选课情况

### 查询任何一门课程成绩在70分以上的姓名、课程名称和分数

### 查询不及格的课程，并按课程号从大到小排列

### 查询课程编号为003且课程成绩在80分以上的学生的学号和姓名

### 求选了课程的学生人数

### 查询选修“叶平”老师所授课程的学生中，成绩最高的学生姓名及其成绩

### 查询各个课程及相应的选修人数

### 查询不同课程成绩相同的学生的学号、课程号、学生成绩

### 查询每门功成绩最好的前两名

### 统计每门课程的学生选修人数（超过10人的课程才统计）。要求输出课程号和选修人数，查询结果按人数降序排列，查询结果按人数降序排列，若人数相同，按课程号升序排列

### 检索至少选修两门课程的学生学号

### 查询全部学生都选修的课程的课程号和课程名

### 查询没学过“叶平”老师讲授的任一门课程的学生姓名

### 查询两门以上不及格课程的同学的学号及其平均成绩

### 检索“004”课程分数小于60，按分数降序排列的同学学号

### 删除“002”同学的“001”课程的成绩