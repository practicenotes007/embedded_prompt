# 嵌入式开发提示工程指南

## 1. 硬件设计提示模板

### 1.1 MCU选型
```prompt
作为一名资深的嵌入式工程师，我需要为[具体应用场景]选择合适的MCU。
需求如下：
- 性能要求：[具体参数]
- 外设需求：[具体外设]
- 功耗要求：[具体要求]
- 成本预算：[具体预算]
请推荐2-3款合适的MCU，并分析其优劣势。
```

### 1.2 外设配置
```prompt
我正在使用STM32F4系列MCU，需要配置以下外设：
- [具体外设1]：[具体需求]
- [具体外设2]：[具体需求]
请提供：
1. CubeMX配置步骤
2. 时钟配置建议
3. 引脚分配建议
4. 可能的注意事项
```

### 1.3 原理图审查
```prompt
请作为资深硬件工程师，审查以下电路设计：
[原理图描述或关键部分]
重点关注：
1. 电源设计
2. 信号完整性
3. EMC考虑
4. 保护电路
请指出潜在问题和优化建议。
```

## 2. 驱动开发提示模板

### 2.1 HAL驱动开发
```prompt
我需要为[具体外设]开发HAL驱动程序。
要求：
1. 基于STM32 HAL库
2. 需要实现的功能：[具体功能列表]
3. 性能���求：[具体要求]
请提供：
1. 关键函数框架
2. 初始化配置代码
3. 错误处理建议
```

### 2.2 传感器驱动
```prompt
我正在开发[具体传感器型号]的驱动程序：
- 通信接口：[具体接口]
- 采样要求：[具体要求]
- 数据格式：[具体格式]
请提供：
1. 驱动程序框架
2. 关键函数实现
3. 校准方法建议
```

## 3. RTOS应用提示模板

### 3.1 任务设计
```prompt
在FreeRTOS环境下，需要设计以下任务：
1. [任务1]：[具体需求]
2. [任务2]：[具体需求]
请提供：
1. 任务优先级分配建议
2. 任务间通信方案
3. 资源竞争处理方法
4. 关键代码框架
```

### 3.2 中断处理
```prompt
需要在RTOS环境下处理以下中断：
- [中断源1]：[处理要求]
- [中断源2]：[处理要求]
请提供：
1. 中断优先级配置建议
2. ISR处理框架
3. 与RTOS任务配合方案
```

## 4. 调试优化提示模板

### 4.1 性能优化
```prompt
我的嵌入式系统存在以下性能问题：
[具体问题描述]
系统参数：
- MCU：[具体型号]
- 时钟配置：[具体配置]
- 关键任务：[具体任务]
请提供优化建议和具体方案。
```

### 4.2 功耗优化
```prompt
需要优化系统功耗，当前情况：
- 工作模式功耗：[具体数值]
- 休眠模式要求：[具体要求]
- 唤醒条件：[具体条件]
请提供：
1. 功耗优化策略
2. 关键代码修改建议
3. 硬件优化建议
```

### 4.3 调试技巧
```prompt
我遇到以下问题：
[具体问题描述]
已经尝试：
1. [尝试方法1]
2. [尝试方法2]
请提供：
1. 可能的原因分析
2. 调试方法建议
3. 解决方案建议
```

## 5. 项目实践提示模板

### 5.1 代码审查
```prompt
请审查以下嵌入式代码：
[代码片段]
重点关注：
1. 代码规范性
2. 潜在bug
3. 性能问题
4. 可靠性考虑
请提供改进建议。
```

### 5.2 架构设计
```prompt
我正在设计一个[具体项目]的嵌入式系统：
- 功能需求：[具体需求]
- 性能要求：[具体要求]
- 硬件限制：[具体限制]
请提供：
1. 系统架构建议
2. 模块划分方案
3. 关键技术选型
4. 潜在风险分析
```

## 使用建议

1. **提示词构建原则**
   - 明确具体场景和需求
   - 提供必要的背景信息
   - 指定期望的输出格式
   - 包含约束条件和限制

2. **优化技巧**
   - 使用专业术语提高准确性
   - 分步骤提问复杂问题
   - 要求具体的代码示例
   - 请求多个可选方案

3. **注意事项**
   - 验证AI生成的代码
   - 关注安全性建议
   - 考虑实际约束
   - 保持迭代优化 

## 6. 代码风格提示模板

### 6.1 C语言代码风格
```prompt
请使用以下代码风格生成C语言代码：

1. 命名规范：
   - 函数名：使用大驼峰命名，如 InitSystem()
   - 变量名：使用小驼峰命名，如 deviceStatus
   - 常量和宏：全大写加下划线，如 MAX_BUFFER_SIZE
   - 类型定义：以_t结尾，如 DeviceConfig_t
   - 枚举值：使用前缀，如 ERR_TIMEOUT

2. 括号和缩进：
   - 左花括号不换行
   - 使用4空格缩进
   - if/for/while等关键字后加空格
   - 函数名和括号间不加空格

3. 注释规范：
   - 文件头部必须包含版权、作者、日期等信息
   - 函数头必须说明功能、参数、返回值
   - 关键算法必须有实现说明
   - 使用统一的注释风格

示例格式：
```c
/**
 * @file    device_driver.c
 * @brief   设备驱动实现
 * @author  Your Name
 * @date    2024-01-01
 * @version 1.0.0
 */

#include "device_driver.h"

#define MAX_RETRY_COUNT    3
#define TIMEOUT_MS         100

typedef struct {
    uint8_t status;
    uint16_t value;
} DeviceData_t;

/**
 * @brief  初始化设备
 * @param  config: 设备配置参数
 * @retval ERR_OK: 成功
 *         ERR_FAIL: 失败
 */
ErrorStatus_t InitDevice(const DeviceConfig_t* config) {
    if (config == NULL) {
        return ERR_INVALID_PARAM;
    }
    
    // 实现代码
    return ERR_OK;
}
```

### 6.2 Python代码风格
```prompt
请使用以下代码风格生成Python代码：

1. 命名规范：
   - 类名：使用大驼峰命名，如 DeviceManager
   - 函数和变量：使用小写加下划线，如 init_device()
   - 常量：全大写加下划线，如 MAX_RETRY_COUNT
   - 私有成员：使用单下划线前缀，如 _private_var

2. 格式规范：
   - 遵循PEP 8规范
   - 使用4空格缩进
   - 最大行长度79字符
   - 类和函数间空两行
   - 方法间空一行

3. 注释规范：
   - 使用文档字符串(docstring)
   - 包含参数和返回值说明
   - 复杂逻辑必须注释
   - 使用类型注解

示例格式：
```python
#!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
设备管理模块

提供设备初始化、配置和控制功能
"""

from typing import Optional, Dict
from dataclasses import dataclass


@dataclass
class DeviceConfig:
    """设备配置数据类"""
    name: str
    port: int
    timeout: float = 1.0


class DeviceManager:
    """设备管理类"""

    def __init__(self, config: DeviceConfig) -> None:
        """
        初始化设备管理器
        
        Args:
            config: 设备配置对象
        """
        self._config = config
        self._is_connected = False

    def connect(self) -> bool:
        """
        连接设备
        
        Returns:
            bool: 连接成功返回True，否则False
        """
        try:
            # 实现代码
            self._is_connected = True
            return True
        except Exception as e:
            print(f"连接失败: {e}")
            return False
```

### 6.3 Java代码风格
```prompt
请使用以下代码风格生成Java代码：

1. 命名规范：
   - 类名：使用大驼峰命名，如 DeviceManager
   - 方法和变量：使用小驼峰命名，如 initDevice()
   - 常量：全大写加下划线，如 MAX_RETRY_COUNT
   - 包名：全小写，如 com.company.project

2. 格式规范：
   - 使用4空格缩进
   - 左花括号不换行
   - 类和方法间空一行
   - 最大行长度120字符

3. 注释规范：
   - 类和公共方法必须有Javadoc
   - 包含@param, @return等标签
   - 关键业务逻辑必须注释
   - 使用统一的注释风格

示例格式：
```java
package com.company.project.device;

import java.util.Optional;
import lombok.Data;

/**
 * 设备管理类
 *
 * @author Your Name
 * @version 1.0.0
 */
@Data
public class DeviceManager {
    private static final int MAX_RETRY_COUNT = 3;
    private static final long TIMEOUT_MS = 1000L;

    private final DeviceConfig config;
    private boolean connected;

    /**
     * 初始化设备
     *
     * @param config 设备配置
     * @return 初始化结果
     * @throws DeviceException 设备异常
     */
    public boolean initDevice(DeviceConfig config) throws DeviceException {
        if (config == null) {
            throw new IllegalArgumentException("Config cannot be null");
        }

        try {
            // 实现代码
            return true;
        } catch (Exception e) {
            throw new DeviceException("Failed to init device", e);
        }
    }
}
```
``` 