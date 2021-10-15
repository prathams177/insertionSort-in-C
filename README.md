# mergeSort-in-C

#include <stdio.h>

void printArray(int *A , int n){
    for(int i=0;i<n;i++){
        printf("%d ",A[i]);
        
    }
    printf("\n");
    
}

void insertionSort(int *A , int n){
    int i,key,j;
    //loop for passes
    for(i=0 ; i<=n-1 ;i++){
        key=A[i];
        j=i-1;
        while(j>=0 && A[j]>key){  //loop for each passes.
            A[j+1]=A[j];
            j--;
            
        }
        A[j+1]=key;
    }
    
    
}



int main()
{
    int A[]={12,54,65,7,23,9};
    int n=6;
   printArray(A,n);//before sort
    insertionSort(A,n);
    printArray(A,n);//after sortt

    return 0;
}
