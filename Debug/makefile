################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
BLMotor_Drive.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
BLMotor_Drive.list \

OBJCOPY_HEX += \
BLMotor_Drive.hex \

OBJCOPY_BIN += \
BLMotor_Drive.bin \


# All Target
all: BLMotor_Drive.elf secondary-outputs

# Tool invocations
BLMotor_Drive.elf: $(OBJS) $(USER_OBJS) C:\Users\Shotaro\ Shimegi\STM32CubeIDE\workspace_1.0.2\BLMotor_Drive\STM32F411RETX_FLASH.ld
	arm-none-eabi-gcc -o "BLMotor_Drive.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\Shotaro Shimegi\STM32CubeIDE\workspace_1.0.2\BLMotor_Drive\STM32F411RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="BLMotor_Drive.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -u _printf_float -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

BLMotor_Drive.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "BLMotor_Drive.list"
	@echo 'Finished building: $@'
	@echo ' '

BLMotor_Drive.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "BLMotor_Drive.hex"
	@echo 'Finished building: $@'
	@echo ' '

BLMotor_Drive.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "BLMotor_Drive.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
