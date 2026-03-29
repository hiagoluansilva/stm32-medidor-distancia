# STM32 Medidor de Distância — Ultrassônico com LCD

🇧🇷 **Português** | 🇺🇸 [English](#english)

---

## Português

Medidor de distância ultrassônico em STM32F4xx com exibição em display LCD, usando captura de tempo via timer.

### O que faz
- Função `disparo()` gera pulso de trigger para sensor HC-SR04
- Captura os tempos `leitura1` e `leitura2` (bordas subindo/descendo do echo)
- Calcula `dif = leitura2 - leitura1` (duração do pulso de eco)
- Converte para centímetros em `conversor()` e exibe em `display()`
- Variáveis: `leitura1`, `leitura2`, `dif`, `contador`, `resultado`

### Funções
```c
void disparo();     // gera pulso trigger de 10 µs
void conversor();   // dif → distância em cm
void display();     // envia resultado para o LCD
```

### Fórmula de distância
```
distância (cm) = (dif × velocidade_do_som) / 2
```

### Hardware necessário
- Sensor ultrassônico **HC-SR04** (ou similar)
- Display LCD (I2C ou paralelo)
- STM32F4xx

---

## English

Ultrasonic distance meter on STM32F4xx with LCD display, using timer-based echo time capture.

### What it does
- `disparo()` generates a trigger pulse for the HC-SR04 sensor
- Captures times `leitura1` and `leitura2` (echo rising/falling edges)
- Computes `dif = leitura2 - leitura1` (echo pulse duration)
- Converts to centimeters in `conversor()` and displays in `display()`
- Variables: `leitura1`, `leitura2`, `dif`, `contador`, `resultado`

### Functions
```c
void disparo();     // generates 10 µs trigger pulse
void conversor();   // dif → distance in cm
void display();     // sends result to LCD
```

### Distance formula
```
distance (cm) = (dif × speed_of_sound) / 2
```

### Required hardware
- **HC-SR04** (or similar) ultrasonic sensor
- LCD display (I2C or parallel)
- STM32F4xx
