#include<stdio.h>
    int main() {
        int  n,i;
        int  A[100];
        printf(" Nhap so phan tu mang:");
	    scanf("%d", &n);
	    for (i = 0; i < n; i++){
		printf("nhap A[%d] :", i);
		scanf("%d", &A[i]);
	}
        int maxsum = 0;
        for (int i = 0; i < n; i++) {
            for (int j = i; j < n; j++) {
                int sum = 0;
                for (int k = i; k <= j; k++)
                    sum += A[k];
                if (sum > maxsum)
                    maxsum = sum;
               
            }
           
        }
        printf("Maxsum: %d", maxsum);
    }
        
   
