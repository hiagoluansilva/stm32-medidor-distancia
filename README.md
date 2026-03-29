# stm32-medidor-distancia

Medidor de distância com sensor ultrassônico HC-SR04 e exibição em display LCD no STM32F4xx.

## Descrição

Sistema que mede a distância até um obstáculo utilizando o sensor ultrassônico HC-SR04, calcula o valor em centímetros e exibe o resultado em um display LCD 16×2. Usa o timer do STM32 para medir o tempo de eco com precisão de microssegundos.

## Hardware

- Microcontrolador: STM32F4xx
- Sensor: HC-SR04 (ultrassônico)
- Display: LCD 16×2

## Princípio de funcionamento

1. Pulso de 10 µs no pino TRIG
2. Medição do tempo do pulso ECHO via input capture do timer
3. Distância = (tempo × velocidade do som) / 2
4. Exibição no LCD

## Estrutura do projeto

```
Medidor_distancia_lcd/
├── Src/
├── Inc/
├── Drivers/
└── Medidor_Distancia_LCD.ioc
```

## IDE

STM32CubeIDE / Atollic TrueSTUDIO

## Escola

Centro Tecnológico Liberato — Novo Hamburgo/RS
