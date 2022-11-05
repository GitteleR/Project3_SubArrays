#include <iostream>
#include <vector>
using namespace std;



//===========================================================
int createSubs()
{
    for (int i = 0; i < n; i++)
    {
        for (int j = i+1; i < n; j++)
        {
            int k = 0;
            inputVect[i] + inputVect[j] = twoDsub[i][k];
            if (i-1 != null)
                {
                    twoDsub[i] = twoDsub[i-1] + twoDsub[i][k];
                }
            k++;
        }

    }
}

//===========================================================
void biggestSubarray (int *biggestX, int *biggestY)
{
    int biggestX = 0;
    int biggestY = 0;

    for (int i = 0; i < n; i++)
    {
        for (int j = i; i < n; j++)
        {
            if (twoDsub[i][j+1] > twoDsub[i][j])
            {
                *biggestX = i;
                *biggestY = j;
            }
        } 

    }

}






int main ()
{

vector <int> inputVect = [];


int twoDsub[n][n];
int indexOne = 0;
int indexTwo = 0;

biggestSubarray(&indexOne, &indexTwo);
cout << "The highest sum value of subarray is: ";

for (int i = indexOne; i <= indexTwo; i++)
{
    cout << inputVect[i] << ", ";
}





return 0;
system("pause");
}
