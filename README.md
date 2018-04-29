# SAMD51---SPI-slaver
目标器件是SAMD51，可以在SAME54开发板上评估该功能
通过SAMD20 Xplaned pro开发板 Master SPI 发送数据给 SAME54 Xplained pro Slaver SPI
//请关注如下SPI PIN口设置 
//PC04 -- SPI 信号输入引脚
void SPI_0_PORT_init(void)
{

	// Set pin direction to input
	gpio_set_pin_direction(PC04, GPIO_DIRECTION_IN);

	gpio_set_pin_pull_mode(PC04,
	                       // <y> Pull configuration
	                       // <id> pad_pull_config
	                       // <GPIO_PULL_OFF"> Off
	                       // <GPIO_PULL_UP"> Pull-up
	                       // <GPIO_PULL_DOWN"> Pull-down
	                       GPIO_PULL_OFF);

	gpio_set_pin_function(PC04, PINMUX_PC04C_SERCOM6_PAD0);

	// Set pin direction to output
	gpio_set_pin_direction(PC05, GPIO_DIRECTION_OUT);

	gpio_set_pin_level(PC05,
	                   // <y> Initial level
	                   // <id> pad_initial_level
	                   // <false"> Low
	                   // <true"> High
	                   false);

	gpio_set_pin_function(PC05, PINMUX_PC05C_SERCOM6_PAD1);

	// Set pin direction to input
	gpio_set_pin_direction(PC06, GPIO_DIRECTION_IN);

	gpio_set_pin_pull_mode(PC06,
	                       // <y> Pull configuration
	                       // <id> pad_pull_config
	                       // <GPIO_PULL_OFF"> Off
	                       // <GPIO_PULL_UP"> Pull-up
	                       // <GPIO_PULL_DOWN"> Pull-down
	                       GPIO_PULL_OFF);

	gpio_set_pin_function(PC06, PINMUX_PC06C_SERCOM6_PAD2);

	// Set pin direction to output
	gpio_set_pin_direction(PC07, GPIO_DIRECTION_OUT);

	gpio_set_pin_level(PC07,
	                   // <y> Initial level
	                   // <id> pad_initial_level
	                   // <false"> Low
	                   // <true"> High
	                   false);

	gpio_set_pin_function(PC07, PINMUX_PC07C_SERCOM6_PAD3);
}


