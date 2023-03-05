
# log4cxx 設定ファイル読み込み

```cpp
#include "log4cxx/xml/domconfigurator.h"

std::string configPath = "c:\\temp\\log4cxx.xml";
log4cxx::xml::DOMConfigurator::configure(configPath);
```
