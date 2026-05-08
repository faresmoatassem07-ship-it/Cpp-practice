#include <iostream>
#include <cmath>
#include <string>
using namespace std;

void Swap(int &a , int &b){
    int temp = a;
    a=b;
    b= temp;
}

void SelectionSort(int arr[],int size){
    int countC=0; //counts number of comparisons
    int countS=0; //counts number of swaps
    
    for (int i =0 ; i<size-1 ; i++){
        int MinIndex=i;
        for(int j=i+1 ; j<size ; j++){
            if(arr[j]<arr[MinIndex]){
                MinIndex=j;
                countC++;
            }
        }
        Swap(arr[MinIndex],arr[i]);
        countS++;
        cout<<"the current array state is: \n";
        for (int z=0 ; z<size ; z++){
            cout  <<arr[z] <<endl;
        }
    }
    cout <<"The count for Total Comparisons: " <<countC;
    cout <<"The count for Total Swaps: " <<countS;
}

int main() {
    
    const int size = 7;
    int Array[7]={3,5,1,8,6,9,4};
    
    SelectionSort(Array,7);
    
    
    return 0;
}
