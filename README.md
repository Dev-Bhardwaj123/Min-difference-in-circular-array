# Min-difference-in-circular-array
Find the minimum difference between adjacent elements in a circular array
//Find min difference for adjacent elements in circular array 
#include<iostream>
#include<bits/stdc++.h>
using namespace std;

int minDiff(int arr[],int n){
	int res=0;
	int mini=abs(arr[1]-arr[0]);
	for(int i=0;i<n;i++){
		res=min(abs(arr[i+1]-arr[i]),mini);
	}
	int m=abs(arr[n-1]-arr[0]);
	res=min(m,res);
	return res;
}

int main(){
	int n;
	cout<<"Enter the size: ";
	cin>>n;
	int arr[n];
	for(int i=0;i<n;i++){
		cin>>arr[i];
	}
	cout<<"Minimum difference is: "<<minDiff(arr,n);
	return 0;
}
