# Hansungproject2018
import csv
a = open('2017_시도별 행정구별 설립별 초등학교수 .csv')
data1 = csv.reader(a)
next(data1)
next(data1)
next(data1)

b = open('201703_201703_연령별인구현황_월간.csv')
data2 = csv.reader(b)
next(data2)

c = open('2017_시도별 행정구별 설립별 초등학교수1.csv')
data3 = csv.reader(c)
next(data3)
next(data3)
next(data3) 

result = []
Gudata = []
popu = []
s = []

for row in data1 :
    c = row[5]
    e = row[0]
    if c != '' : #공집합 제거
        if e == '서울' : #전국 데이터에서 서울시만 선택
            result.append(int(c)) #서울시 각 구별 초등학교 수
            
for row in data2 :
    popu.append(int(row[2])) #서울시 각 구별 초등학생 수

plt.savefig('서울 각 구 별 인구대비 학교수.png')
plt.show()
