# queue
# c
첫째줄의 명령수와 그다음줄부터 명령어를 입력하고 결과를 출력하는 프로그램을 작성해보자!

#include <stdio.h>
#include <stdlib.h> 
#include <string.h>

int q[1000];
int start=0,end=0,cnt=0;

void push(int x){
	q[end++]=x;
	cnt++; }
	
	
void pop(){
	if(cnt!=0){
		printf("%d\n",q[start++]);
		cnt--;}
	else printf("이미 비어있다!\n"); }
	
	
void size(){
	printf("%d\n",cnt); }
	
	
void empty(){
	if(cnt!=0){
		printf("비어있지않다!\n");}
	else{
		printf("비어있다!");} }
		
		
void front(){
	if(cnt!=0){
		printf("%d\n",q[start]);}
	else printf("들어있는 수가 없다!\n"); }
	
	
void back(){
	if(cnt!=0){
		printf("%d\n",q[end-1]);}
	else printf("들어있는 수가 없다!\n"); }
	
	
void main(){
	int n,i,x;
	scanf("%d",&n);
	for(i=0;i<n;i++){
		char c[100];
		scanf("%s",&c);
		if(!strcmp(c,"push")){
			scanf("%d",&x);
			push(x);}
		else if(!strcmp(c,"pop")){
			pop();}
		else if(!strcmp(c,"size")){
			size();}
		else if(!strcmp(c,"empty")){
			empty();}
		else if(!strcmp(c,"front")){
			front();}
		else if(!strcmp(c,"back")){
			back();} }  }
