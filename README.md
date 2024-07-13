# vscode_embedded

Some useful embededd systems related vscode configurations to make embedded development setup easier.
Soon there will be configurations for zephyr and nuttx.
For esp idf and stm32 development, there are already working extensions, but there might be something about those too.

For each configurations I've put an extensions.json file containing the necessary extensions to install.

For both zephyr and nuttx gdb-multiarch should be installed.

Notes:

- zephyr:
  
  - The configurations needs an environment script like the one provided, replace the path \$HOME/.zephyr_setup with the path to your script location, I usually define the board in the project's cmakelists.txt with set(BOARD nucleo-f446re) as an example

- nuttx:
  
  - There's already an extension for nuttx development(it can be found in the extensions.json), so I've only added the necessary extensions and a two debugging configurations, one of them is with the built in debug feature of the cpp tools extension from microsoft, the other uses cortex debug, I have found native debug to be pretty useless given the built in debugging capability of cpp tools. The cortex debug extension instead, provides better debugging functionality access(global variables are visible and there's no need to use watch, even though it is probably best) and slightly snappier performance
