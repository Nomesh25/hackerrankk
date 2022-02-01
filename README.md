# hackerrankk
#include <bits/stdc++.h>
using namespace std;
int arraySum(vector<int> &v)
{
    int initial_sum = 0;
    return accumulate(v.begin(), v.end(), initial_sum);
}
void remove(int arr[], int n, int t)
{
    int temp[n];
    for (int i = 0; i < n; i++)
    {
        int j = 0;
        if (arr[i] >= t)
        {
            temp[j++] = arr[i];
        }
    }

    int size = sizeof(temp)/sizeof(temp[0]);
    int diff[size];
    for(int i=0;i<size;i++){

        diff[i]=temp[i]-t;


    }
}
int main()
{
    int n;
    cin >> n;
    vector<int> arr(n);
    for (int i = 0; i < n; i++)
    {
        cin >> arr[i];
    }
    int sum1 = arraySum(arr);
    sort(arr.begin(), arr.end());
    int avg = sum1 / n;
    cout << avg;
    int j = 0;
    int temp[3];
    for (int i = 0; i < n; i++)
    {
        if (arr[i] >= avg)
        {
            temp[j++] = arr[i];
        }
    }
    for (int i = 0; i < 3; i++)
    {

        cout << temp[i] << endl;
    }

    return 0;
}
