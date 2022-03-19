# Codeforcescpp-462A
#include <bits/stdc++.h>
 
using namespace std;
 
int main(){
  int n;
  cin >> n;
  string s[101];
  for(int i=0;i<n;i++){
    cin >> s[i];
  }
  int c=0;
  for(int i=0;i<n;i++){
    int count = 0;
    for(int j=0;j<n;j++){
      if(i > 0 && s[i-1][j]=='o'){
        count++;
      }
      if(i < n-1 && s[i+1][j]=='o'){
        count++;
      }
      if(j > 0 && s[i][j-1]=='o'){
        count++;
      }
      if(j < n-1 && s[i][j+1]=='o'){
        count++;
      }
      if((count%2)==0){
        c++;
      }
      else{
        cout << "NO";
        return 0;
      }
    }
    
  }
  cout << "YES";
  return 0;
}
