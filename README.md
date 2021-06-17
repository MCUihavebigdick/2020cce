# 2020cce
# 2020cce
## 進階題:分式化簡
```C
#include <stdio.h>
int main()
{
	int m,n,i;
	scanf("%d%d" ,&m, &n);
	for(int i=m;i>=1;i--)
	{
		if((m%i==0)&&(n%i==0))
		{
			m=m/i;
			n=n/i;
		}
	}
	printf("%d %d\n",m,n);
	return 0;
}
```
## 進階題：讀入整數反序列印
```C
#include <stdio.h>
int main()
{
	int m,n,i;
	scanf("%d%d" ,&m, &n);
	for(int i=m;i>=1;i--)
	{
		if((m%i==0)&&(n%i==0))
		{
			m=m/i;
			n=n/i;
		}
	}
	printf("%d %d\n",m,n);
	return 0;
}
```
## 進階題：A的B次方函數
```C
#include <stdio.h>
int main()
{
	int m,n,i;
	scanf("%d%d" ,&m, &n);
	for(int i=m;i>=1;i--)
	{
		if((m%i==0)&&(n%i==0))
		{
			m=m/i;
			n=n/i;
		}
	}
	printf("%d %d\n",m,n);
	return 0;
}
```
## 進階題：漸增數列相加 
```C
#include <stdio.h>
int main()
{
	int a,n=0;
	scanf("%d", &a);
	for(int i=2;i<=a;i++)
	{
		int j,z;
		j=i-1;
		z=j*i;
		n=n+z;
	}
	printf("%d\n",n);
}
```
## 基礎題：找零錢
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	printf("%d=50*%d+5*%d+1*%d\n",n,n/50,n%50/5,n%50%5);
}
```
## 基礎題：因數個數
```C
#include <stdio.h>
int main()
{
	int a;
	scanf("%d",&a);
	int k=0;
	for(int i=1;i<=a;i++){
		if(a%i==0){
			k++;
		}
	}
	printf("%d\n",k);
}
```
## 基礎題：找倍數 
```C
#include <stdio.h>
int main()
{
	int a,k=0;
	for(int i=1;i<=10;i++){
		scanf("%d",&a);
		if(a%3==0){
			k++;
		}
	}
	printf("%d\n",k);
}
```

## 基礎題：整數轉換為等級 
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	if(n>=90)printf("A\n");
	else if(n>=80)printf("B\n");
	else if(n>=60)printf("C\n");
	else if(n<60)printf("F\n");
}
```
```C
13-1
void setup(){
  size(1024,400);
}
void draw(){
  if (mousePressed) background(51,146,203); 
  else background(51,203,128);
}
```
```C
13-2
size(1024,400) 
 background(51,203,128);
```
```C
13-3
void setup(){//只做一次設定
  size(1024,400);
}
void draw(){//互動版本每秒畫60次
  if (mousePressed) background(51,146,203); //按下去淺藍
  else background(51,203,128);//否則淺綠
14-1
void setup(){//設定只做一次
float ans= random(60);//亂數 會是<60的浮點數
text(ans,20,20);//畫出ans
}
void draw(){//畫圖 每秒60次

}
14-2
int ans=0;
void setup(){//設定只做一次
//  float ans= random(60);//亂數 會是<60的浮點數
  size(300,300);
  textSize(30);
}
void draw(){//畫圖 每秒60次
background(#62AED3);
text(ans,20,30);
}
  void mousePressed(){//按下去 互動一次
    ans = (int)random(60);//浮點數不能直接變整數
}
14-3
int []a={1,2,3,4,5,6,7,8,9,10};//Java
int i1,i2;
void setup(){
  size(400,100);
  textSize(30);
  }
 void draw(){
   background(#62AED3);
   for(int i=0;i<10;i++){
     text(a[i],i*40,50);
   }
   rect(i1*40,50,30,30);
   rect(i2*40,50,30,30);
 }
 void mousePressed(){
   for(int i=0;i<100;i++);{
     i1=(int)random(10);
     i2=(int)random(10);
     int temp=a[i1];a[i1]=a[i2];a[i2]=temp;
   }
 }
14-4
int []a=new int[47];//JAVA陣列
void setup(){
  size(500,200);//大一點
  textSize(30);
  for(int i=0;i<47;i++)a[i]=i;
//讓a[i]的陣列裡面要先放整齊對應的數字
  for(int i=0;i<1000;i++){
    int i1 = (int)random(47);
    int i2 = (int)random(47);
    int temp=a[i1];a[i1]=a[i2];a[i2]=temp;
  }//作弊 先洗好牌 先知道得獎號碼 等下再掉出來
}
void draw(){
  background(#62AED3);
  for(int i=0;i<5;i++){
    text(a[i],i*80,100);
  }
}
14-5
int []a=new int[47];//JAVA陣列
void setup(){
  size(500,200);//大一點
  textSize(30);
  for(int i=0;i<47;i++)a[i]=i;
//讓a[i]的陣列裡面要先放整齊對應的數字
  for(int i=0;i<1000;i++){
    int i1 = (int)random(47);
    int i2 = (int)random(47);
    int temp=a[i1];a[i1]=a[i2];a[i2]=temp;
  }//作弊 先洗好牌 先知道得獎號碼 等下再掉出來
}
int N=0;
void draw(){
  background(#62AED3);
  for(int i=0;i<N;i++){
    text(a[i],i*80,100);
  }
}
void mousePressed(){
  N++;
}
14-6
int []a=new int[47];//JAVA陣列
void setup(){
  size(500,200);//大一點
  textSize(30);
  for(int i=0;i<47;i++)a[i]=i;
//讓a[i]的陣列裡面要先放整齊對應的數字
  for(int i=0;i<1000;i++){
    int i1 = (int)random(47);
    int i2 = (int)random(47);
    int temp=a[i1];a[i1]=a[i2];a[i2]=temp;
  }//作弊 先洗好牌 先知道得獎號碼 等下再掉出來
}
int N=0;
void draw(){
  textAlign(CENTER,CENTER);//文字對齊:中.中
  background(#62AED3);
  for(int i=0;i<N;i++){
    fill(255); ellipse(    i*80+40,100,55,55);
    fill(0);     text(a[i],i*80+40,100);
  }
}
void mousePressed(){
  N++;
}
15-1
//自動打鐘的程式
void setup(){
  size(400,200);
}
void draw(){
  int s= second();//0...59秒
  if(s%2==0) background(#50C5E8);
  else background(#50E8A9);
}
15-1(2)
void setup(){
  size(400,200);
  textSize(40);//大字
}
void draw(){
  int s= second();//s會增加0...59
  background(#50C5E8);
 // text(59-s,100,100);//59....1減少
  text(10-s%11,100,100);//10.9.8.7...3.2.1.0,共11個數
}
15-3
import processing.sound.*;
SoundFile player;
void setup(){
  size(400,200);
  player = new SoundFile(this, "tada.mp3");
}
void draw(){
  background(#50C5E8);
}
void mousePressed(){
  player.play();
}
15-4
點擊播放 點擊停止
import processing.sound.*;
SoundFile player;
void setup(){
  size(400,200);
  player = new SoundFile(this, "bell.mp3");
}
void draw(){
  background(#50C5E8);
}
void mousePressed(){
  if(player.isPlaying()){
  player.stop();  
  }else{
    player.play();//太吵了
  }
}
15-5 tada
import processing.sound.*;
SoundFile player;
void setup(){
  size(400,200);
  textSize(40);//大字
  player = new SoundFile(this, "tada.mp3");
}
void draw(){
  int s= second();//s會增加0...59
  background(#50C5E8);
 // text(59-s,100,100);//59....1減少
  text(10-s%11,100,100);//10.9.8.7...3.2.1.0,共11個數
  if(10-s%11==0 && !player.isPlaying()){
    player.play();
  }
}
15-6
function setup() {
  createCanvas(400,200);
}
function draw() {
    let s = second();
    if(s%2==0){
      background(255,0,0);
    }else{
      background(58,114,191);
    }
    
}
16-1
void setup(){
  size(400,200);
}
void draw(){
  background(#6FF5BA);
  ellipse (50,50,80,80);
//       圓心, 寬,高 
}
16-2
void setup(){
  size(400,200);
}
void draw(){
  background(#6FF5BA);
  fill(255);
  ellipse (50,50,80,80);
//       圓心, 寬,高 
  fill(#53A4CE);
  float stop=mouseX/50.0;
  text(stop,100,100);//劃出弧度
  arc(50,50,80,80,0,stop);
  //  圖心  寬高 開始 結束
}
16-3
void setup(){
  size(400,200);
}
void draw(){
  background(#6FF5BA);
  fill(255);
  ellipse (50,50,80,80);
//       圓心, 寬,高 
  fill(#53A4CE);
  float start=mouseX/50.0;
  textSize(40);
  text(start,100,100);
  arc(50,50,80,80,0+start,0.1+start);
  //  圖心  寬高 開始 結束
}
16-4
void setup() {
  size(400, 200);
}
void draw() {
  background(#B389EA);
  fill(255);
  ellipse(100, 100, 180, 180);

  fill(255, 0, 0);
  float start=mouseX/50.0;
  for (int i=0; i<24; i++) {
    float shift=2*PI*i/24.0;
    if (i%3==0) fill(255);
    if (i%3==1) fill(#FFF86C);
    if (i%3==2) fill(#89D0EA);
    arc(100, 100, 180, 180, shift+0+start, shift+PI/12+start);
  }
}
16-5
void setup() {
  size(400, 200);
}
void draw() {
  background(#B389EA);
  fill(255);
  ellipse(100, 100, 180, 180);

  fill(255,0,0);
  float start=mouseX/50.0;
  for (int i=0; i<24; i++) {
    float shift=2*PI*i/24.0;
    if (i%3==0) fill(255);
    if (i%3==1) fill(#FFF86C);
    if (i%3==2) fill(#89D0EA);
    if(i==0) fill(#FA761E);
    arc(100, 100, 180, 180, shift+0+start, shift+PI/12+start);
  }
}
16-6
void setup() {
  size(400, 200);
}
float start=0;
void draw() {
  background(#B389EA);
  if(start <10) start+=0.01;// float start=mouseX/50.0;
  fill(255);
  text(start,200,150);
  for (int i=0; i<24; i++) {
    float shift=2*PI*i/24.0;
    if (i%3==0) fill(255);
    if (i%3==1) fill(#FFF86C);
    if (i%3==2) fill(#89D0EA);
    if(i==0) fill(#FA761E);
    arc(100, 100, 180, 180, shift+0+start, shift+PI/12+start);
  }
}
16-7
void setup() {
  size(400, 200);
}
float start=0,v=0.07;
void draw() {
  background(#B389EA);
  if(v>0.001){
  start +=v;//位置 速度 加速度 (位置會加上速度)
  v*=0.99;//摩擦力為讓速度變慢 位置 速度 加速度(速度加上加速度)
  }
 // if(start <10) start+=0.01;// float start=mouseX/50.0;
  fill(255);
  text(start,200,150);
  text(v,200,170);
  for (int i=0; i<24; i++) {
    float shift=2*PI*i/24.0;
    if (i%3==0) fill(255);
    if (i%3==1) fill(#FFF86C);
    if (i%3==2) fill(#89D0EA);
    if(i==0) fill(#FA761E);
    arc(100, 100, 180, 180, shift+0+start, shift+PI/12+start);
  }
}
16-8
void setup() {
  size(400, 200);
}
float start=0,v;
void mousePressed(){
  v = random(1);
}
void draw() {
  background(#B389EA);
  if(v>0.001){
  start +=v;//位置 速度 加速度 (位置會加上速度)
  v*=0.99;//摩擦力為讓速度變慢 位置 速度 加速度(速度加上加速度)
  }
 // if(start <10) start+=0.01;// float start=mouseX/50.0;
  fill(255);
  text(start,200,150);
  text(v,200,170);
  for (int i=0; i<24; i++) {
    float shift=2*PI*i/24.0;
    if (i%3==0) fill(255);
    if (i%3==1) fill(#FFF86C);
    if (i%3==2) fill(#89D0EA);
    if(i==0) fill(#FA761E);
    arc(100, 100, 180, 180, shift+0+start, shift+PI/12+start);
  }
}
17-1
void setup(){
  size(400,200);
  textSize(40);
}
String line="hello";
void draw(){
  background(#8FF0D3);
  text(line,100,100);//可以將字串LINE畫出來
  text("World",100,150);//也可以印出來
}
void setup(){
  size(400,200);
  textSize(40);
}
String line="hello";
char c='9';
void draw(){
  background(#8FF0D3);
  text(line+c+100,100,100);//可以將字串LINE畫出來
  text("World:"+key,100,150);//也可以印出來
}//這裡發現 字串的+其實是越加越長
//key會對應你最後按下的(字母.數字.符號)
17-3
void setup(){
  size(400,200);
  textSize(40);
}
char c='9';
int win=0;
void draw(){
  background(#8FF0D3);
  text("Pressed:"+c,100,100);
  text("You :"+key,100,150);
  if(c==key) win=1;
  else win=0;
  
  if(win==1) text("You win!",100,50);
}
17-4
void setup(){
  size(400,200);
  textSize(40);
}
char c='9';
String ans = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ";
int win=0;
void draw(){
  background(#8FF0D3);
  text("Pressed:"+c,100,100);
  text("You :"+key,100,150);
  if(c==key) win=1;
  else win=0;
  
  if(win==1){
  text("You win!",100,50);
  int i = int(random(26+26));
  c = ans.charAt(i);
  }
 }
17-5
void setup(){
  size(400,200);
   textSize(40);
}
int x=100,y=100;
void draw(){
  background(#8FF0D3);
  rect(x,y,50,50);
}
void keyPressed(){
   if(keyCode==LEFT) x-=10;
   if(keyCode==RIGHT)x+=10;
 }
17-6
void setup(){
  size(400,200);
   textSize(40);
}
int x=100,y=100,vx=0,vy=0;
void draw(){
  background(#8FF0D3);
  rect(x,y,50,50);
  x += vx;
}
void keyPressed(){
   if(keyCode==LEFT) vx=-1;
   if(keyCode==RIGHT)vx=+1;
 }
 void keyReleased(){
   vx=0;
 }
17-7
String A="mother";
String line="";

void setup(){
  size(400,300);
  textSize(40);
}
void draw(){
  background(0);
  text(A,100,100);
  text(line +"|",100,150);
}
void keyPressed(){
  line = line + key;
}
17-8
String A="mother";
String line="";

void setup(){
  size(400,300);
  textSize(40);
}
void draw(){
  background(0);
  text(A,100,100);
  text(line +"|",100,150);
}
void keyPressed(){
  int len = line.length();
  if(key>='a' && key<='z')line = line + key;
  if(key>='A' && key<='Z')line = line + key;
  if(key==ENTER){    }
  if(key==BACKSPACE && len>0) line = line.substring(0, len-1);
}
