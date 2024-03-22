# freertos-project
这是一个stm32移植freertos的程序，但是我移植之后发现模拟仿真可以正常运行，但是烧写到单片机上就不可以了，程序卡死在LDR RO, =SystemInit。stm32f03c8t6
最后查出来是内存堆分配的太大了，#define configTOTAL_HEAP_SIZE		( ( size_t ) (8 * 1024 ) )将他改成这个就行了
