## 使用方式
1. 在 https://github.com/ricofx2003/miui-hosts/releases 下载最新的 miui-hosts.zip。
2. 在 magisk 中安装并重启。

## 参考
https://github.com/Moe-hacker/FuckMIUI  
https://github.com/LoopDns/Fuck-you-MIUI  
https://github.com/yuk7/miui12-fontsxml

## 整理
主要是去重。源代码如下：
```cpp
#include <bits/stdc++.h>
using namespace std;
using ll = long long;

int main() {
    freopen("hosts", "r", stdin);
    freopen("_hosts", "w", stdout);
    map<string, bool> m;
    string s;
    while (getline(cin, s)) {
        if (s.substr(0, 1) == "#" ||  m.count(s)) continue;
        m[s] = 1;
        cout << s << endl;
    }
    return 0;
}
```