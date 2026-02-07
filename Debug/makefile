################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (13.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := LED_TOGGLE_USING_REGISTOR
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
LED_TOGGLE_USING_REGISTOR.elf \

MAP_FILES += \
LED_TOGGLE_USING_REGISTOR.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
LED_TOGGLE_USING_REGISTOR.list \

OBJCOPY_HEX += \
LED_TOGGLE_USING_REGISTOR.hex \

OBJCOPY_BIN += \
LED_TOGGLE_USING_REGISTOR.bin \


# All Target
all: main-build

# Main-build Target
main-build: LED_TOGGLE_USING_REGISTOR.elf secondary-outputs

# Tool invocations
LED_TOGGLE_USING_REGISTOR.elf LED_TOGGLE_USING_REGISTOR.map: $(OBJS) $(USER_OBJS) C:\Users\piyush\STM32CubeIDE\workspace_2.0.0\LED_TOGGLE_USING_REGISTOR\STM32F103C8TX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "LED_TOGGLE_USING_REGISTOR.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\piyush\STM32CubeIDE\workspace_2.0.0\LED_TOGGLE_USING_REGISTOR\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="LED_TOGGLE_USING_REGISTOR.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

LED_TOGGLE_USING_REGISTOR.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "LED_TOGGLE_USING_REGISTOR.list"
	@echo 'Finished building: $@'
	@echo ' '

LED_TOGGLE_USING_REGISTOR.hex: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "LED_TOGGLE_USING_REGISTOR.hex"
	@echo 'Finished building: $@'
	@echo ' '

LED_TOGGLE_USING_REGISTOR.bin: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "LED_TOGGLE_USING_REGISTOR.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) LED_TOGGLE_USING_REGISTOR.bin LED_TOGGLE_USING_REGISTOR.elf LED_TOGGLE_USING_REGISTOR.hex LED_TOGGLE_USING_REGISTOR.list LED_TOGGLE_USING_REGISTOR.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
