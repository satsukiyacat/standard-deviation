#include<bits/stdc++.h>
#define rep(i, m, n) for(int i = m; i < (int)(n); i++)
#define _GLIBCXX_DEBUG
using namespace std;
using ll = long long;

int main() {
    double n;
    cin >> n;
    vector<int> data(n);

    double sum = 0;
    rep(i, 0, n) {
        cin >> data[i];
        sum += data[i];
    }

    sort(data.begin(), data.end());
    
    double ave = sum / n;
    
    double devsumsqrt = 0;
    rep(i, 0, n) {
        devsumsqrt += (data[i] - ave) * (data[i] - ave);
    }

    double varp = devsumsqrt / n;
    double standdev = sqrt(varp);

    double lefto = 0;
    double righto = n;
    bool richange = false;
    while(righto - lefto > 1) {
        if(!richange) {
            righto = (lefto + righto) / 2;
            richange = true;
        } 
        else if(richange) {
            lefto = (lefto + righto) / 2;
            richange = false;
        }
    }
    double qone = (data[righto] + data[lefto]) / 2;

    double leftt = 0;
    double rightt = n;
    bool lechange = false;
    while(rightt - leftt >1) {
        if(!lechange) {
            leftt = (leftt + rightt) / 2;
            lechange = true;
        }
        else if(lechange) {
            rightt = (leftt + rightt) / 2;
            lechange = false;
        }
    }
    double qthree = (data[rightt] + data[leftt]) / 2;

    double quartdev = (qthree - qone) / 2;

    cout << varp << " " << standdev << " " << quartdev << endl;
}
