# f411_piocube_lib_blink
project integrating cubemx in platformio as a library so that clock and HAL init are taken care of and the user can focus on the application

# Use CubeMX like Arduino
Although no construction style is possible as the main compiled by the cubemx lib has to run first, so init has to follow starting on the `setup()` function.

It's really the `stm32cube` framework
```ini
[env]
platform = ststm32
framework = stm32cube

```
The library can be added with the repository url
```ini
lib_deps =
    https://github.com/STM32Libs/pio_cubemx_stm32f4.git

```
`main.cpp` looks like Arduino `.ino` file
```cpp
#include "cube_main.h"

void setup()
{
	//init led
}

void loop()
{
    //blink led
}

```
