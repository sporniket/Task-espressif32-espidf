# Task-espressif32-espidf
C++ library for PlatformIO, provides the wrapper class 'Task' taken from https://github.com/nkolban/esp32-snippets.

## LICENSE

GPL v3

## What's new

### v0.0.2

* adapt to recent idf version

### v0.0.1

Initial publishing, extracted from working code.


## Typical application

_See also [the showcase/maintenance project](https://github.com/sporniket/demo-task-gpio-button-led)_

```cpp
#include "Task.h"
// ...

class LedUpdaterTask : public Task {
    public:
        //...
        void run(void *data) {
            const TickType_t SLEEP_TIME = 100 / portTICK_PERIOD_MS ; // 10 Hz
            //...
            while(true) {
                //...
                vTaskDelay(SLEEP_TIME);
            }
            
        }
} ;

```