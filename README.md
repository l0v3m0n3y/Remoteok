# Remoteok
api for remoteok.com site for getting romote jobs
# main
```cpp
#include "Remoteok.h"
#include <iostream>

int main() {
   Remoteok api;
    auto job = api.get_remote_job().then([](json::value result) {
        std::cout << result<< std::endl;
    });
    job.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
