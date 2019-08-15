################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
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
ArduinoToSTM32_13.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
ArduinoToSTM32_13.list \


# All Target
all: ArduinoToSTM32_13.elf secondary-outputs

# Tool invocations
ArduinoToSTM32_13.elf: $(OBJS) $(USER_OBJS) /home/twistx77/STM32CubeIDE/workspace_1.0.0/ArduinoToSTM32_13/STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "ArduinoToSTM32_13.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/twistx77/STM32CubeIDE/workspace_1.0.0/ArduinoToSTM32_13/STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="ArduinoToSTM32_13.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

ArduinoToSTM32_13.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "ArduinoToSTM32_13.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
