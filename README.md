# Coding-solution2
Question link :- https://codeforces.com/problemset/problem/1472/B

Submission link :- https://codeforces.com/contest/1472/submission/112189060

Source code :- 

            #include<iostream>
            using namespace std;
            int main()
            {
                int t;
                cin>>t;
                while(t--){
                    int n;
                    cin>>n;
                    int arr[n];
                    int oneGram = 0, twoGram = 0;
                    for(int i=0;i<n;i++){
                        cin>>arr[i];
                        if(arr[i] == 1){
                            oneGram++;
                        }
                        else{
                            twoGram++;
                        }
                    }
                    int first = arr[0], second = arr[1];
                    for(int i=2;i<n;i++){
                        if(first > second){
                            second += arr[i];
                        }
                        else{
                            first += arr[i];
                        }
                    }
                    if(oneGram%2==0 && twoGram%2==0 || oneGram%2==0 && twoGram%2!=0 && oneGram>0){
                        cout<<"YES"<<endl;
                    }
                    else{
                        cout<<"NO"<<endl;
                    }
                }
                return 0;
            }
