################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (13.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/MemMang/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/GCC/ARM_CM7/r0p1/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS_V2/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/subdir.mk
-include Drivers/STM32F7xx_HAL_Driver/Src/subdir.mk
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


BUILD_ARTIFACT_NAME := ATIVIDADE-AULA04-EXERCICIO04-TILM
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
ATIVIDADE-AULA04-EXERCICIO04-TILM.elf \

MAP_FILES += \
ATIVIDADE-AULA04-EXERCICIO04-TILM.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
ATIVIDADE-AULA04-EXERCICIO04-TILM.list \


# All Target
all: main-build

# Main-build Target
main-build: ATIVIDADE-AULA04-EXERCICIO04-TILM.elf secondary-outputs

# Tool invocations
ATIVIDADE-AULA04-EXERCICIO04-TILM.elf ATIVIDADE-AULA04-EXERCICIO04-TILM.map: $(OBJS) $(USER_OBJS) C:\Users\robso\OneDrive\Documentos\Cube_ide_2\ATIVIDADE-AULA04-EXERCICIO04-TILM\STM32F767ZITX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "ATIVIDADE-AULA04-EXERCICIO04-TILM.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m7 -T"C:\Users\robso\OneDrive\Documentos\Cube_ide_2\ATIVIDADE-AULA04-EXERCICIO04-TILM\STM32F767ZITX_FLASH.ld" --specs=nosys.specs -Wl,-Map="ATIVIDADE-AULA04-EXERCICIO04-TILM.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv5-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

ATIVIDADE-AULA04-EXERCICIO04-TILM.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "ATIVIDADE-AULA04-EXERCICIO04-TILM.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) ATIVIDADE-AULA04-EXERCICIO04-TILM.elf ATIVIDADE-AULA04-EXERCICIO04-TILM.list ATIVIDADE-AULA04-EXERCICIO04-TILM.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
