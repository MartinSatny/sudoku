#include <iostream>
#include <stdio.h>
#include <vector>

using namespace std;

int printSudoku(int arr[9][9]) {
  cout << "---------------" << endl;

  for (int r = 0; r < 9; r++){
    for (int c = 0; c < 9; c++)
        cout << arr[r][c] << " ";
    cout << endl;
  }
  cout << "---------------" << endl;
}

bool canPlace(int arr[9][9], int row, int col, int num) {
    if (arr[row][col] != 0) return false;
  bool status = true;
  int gridx = (col / 3) * 3;
  int gridy = (row / 3) * 3;
  for (int i = 0; i < 9; i++) {
    if(arr[row][i] == num){status = false; break;}
    if(arr[i][col] == num){status = false; break;}
    if(arr[gridy + i / 3][gridx + i % 3] == num){status = false; break;}
} return false;
}
vector<int> findPlacebles(int arr[9][9], int row, int col) {
  vector<int> cps ={};
  for (int i = 1; i <= 9; i++) {
    if(canplace(arr, r, c, i)) 
      cps.push_back(i);
}
  return cps;
}
void copyArray (int arr[9][9], int arrCpy[9][9]){
  for(int y=0; y<9; y++)
    for(int x=0; x<9l; x++)
      arrCpy[y][x] = arr[y][x];
}
void nextEmpty(int arr[9][9], int rowm, int col, int nextRow, int nextCol){
  int index = 9 * 9;
}
bool solveSudoku(int arr[9][9], int row, int col) {
  if (row == 9 - 1 && col == 9) return true;
  vector<int> placebles = findPlacebles(arr, row, col);
  if(placebles.size() == 0) return false;
  bool status = false;
  for (int i =0; i < placebles.size(); i++){
    int num = placebles[i];
    int arrCpy[9][9];
    copyArray(arr, arrCpy);
    arrCpy[row][col] = num;
    int nextCol, nextRow;
    if(solveSudoku(arrCpy, nextCol, nextRow)){
      copyArray(arrCpy, arr);
      status = true;
      break;
    }
  }
}
int main(){
   int board [9][9] = {
   
   {0, 0, 4, 0, 0, 0, 0, 0, 0},
   {0, 0, 0, 0, 0, 0, 0, 0, 0},
   {0, 0, 0, 0, 0, 0, 0, 0, 0},
   {0, 0, 0, 0, 0, 0, 0, 0, 0},
   {0, 0, 0, 0, 0, 0, 0, 0, 0},
   {0, 0, 0, 0, 0, 0, 0, 0, 0},
   {0, 0, 0, 0, 0, 0, 0, 0, 0},
   {0, 0, 0, 0, 0, 0, 0, 0, 0},
   {0, 0, 0, 0, 0, 0, 0, 0, 0}
   };
   printSudoku(board);
return 0;
}


