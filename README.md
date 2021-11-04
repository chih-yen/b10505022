# b10505022 HW
#include <stdio.h>

int main()
{

int num[4][4];
int i,j;
for(i = 0; i < 4; i++)
{
    for(j = 0; j < 4; j++)
    {
        scanf("%d",&num[i][j]);
    }
}

for(i = 0; i < 4; i++)
{
    for(j = 0; j < 4; j++)
    {
        printf("%2d",num[i][j]);
        if(j != 3)
        {
            printf(" ");
        }
    }
    printf("\n");
}
printf("\n");

int row[4],col[4];
for(i = 0; i < 4; i++)
{
    row[i] = 0;
    col[i] = 0;
    for(j = 0; j < 4; j++)
    {
        row[i] += num[i][j];
        col[i] += num[j][i];
    }
}
int dia[2];
dia[0] = num[0][0] + num[1][1] + num[2][2] + num[3][3];
dia[1] = num[0][3] + num[1][2] + num[2][1] + num[3][0];

printf("Row sums: %2d %2d %2d %2d\n",row[0],row[1],row[2],row[3]);
printf("Column sums: %2d %2d %2d %2d\n",col[0],col[1],col[2],col[3]);
printf("Diagonal sums: %2d %2d\n",dia[0],dia[1]);

return 0;
}
