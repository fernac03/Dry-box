# Instruções

Eu queria uma caixa desumidificadora (drybox) que fosse o mais acessível possível, sem abrir mão de funcionalidades!

Já existem muitos projetos por aí que utilizam o conhecido pote para cereais como base, mas nenhum deles atende a todos os meus critérios. Eu quis mudar isso.

# Características:
Baixo consumo de material, apenas ~360g de filamento para  acomodar  4 rolos
Etiquetas substituíveis e personalizáveis
Higrômetro
Rolamentos para guiar a bobina
Também compatível com bobinas de até 70mm de largura
recipiente secundário opcional

A caixa é feita de PP (polipropileno), um material que impede a passagem de umidade, sendo, portanto, ideal para uma caixa de armazenamento a seco (dry box). São necessários apenas um ou dois furos de 10mm para o tubo de PTFE (dependendo se você deseja usar dois conectores — um para a guia de filamento e outro para guardar o tubo após removê-lo da impressora).

# O que você vai precisar:
16x rolamentos 5x16x5 (modelo 625zz / 625-2RS)
16x parafusos M5x16-20mm (cabeça abaulada, panela ou arredondada)
4 a 8x conectores pneumáticos PC4-M10
1x Caixa Plasutil 29L 
1 Wemos d1 Mini
1 sensor SHT40X
~360g de filamento (recomenda-se PETG ou PCTG) 
Tubo de PTFE de 4mm (recomenda-se diâmetro interno de 2,5mm)
Broca de 10mm (recomenda-se uma broca escalonada)
Sílica gel

# Opcional
1 x Módulo de Display OLED de 0,91 Polegadas I2C 128x32 para


### 📋 Tabela de Conexões (Pinout)

Como tanto o sensor quanto o display utilizam o protocolo de comunicação I2C, eles compartilham o mesmo barramento (pinos de dados e clock) conectados em paralelo no Wemos D1 Mini.

| Componente | Pino do Componente | Pino no Wemos D1 Mini | Tipo de Sinal / Função |
| :--- | :--- | :--- | :--- |
| **Sensor SHT40** | VCC | 3V3 | Alimentação Positiva (3.3V) |
| | GND | GND | Referência de Terra (0V) |
| | SDA | D2 (GPIO4) | Linha de Dados I2C (*Serial Data*) |
| | SCL | D1 (GPIO5) | Linha de Clock I2C (*Serial Clock*) |
| **Display OLED 0.91"** <br>*(Opcional)* | VCC | 3V3 | Alimentação Positiva (3.3V) |
| | GND | GND | Referência de Terra (0V) |
| | SDA | D2 (GPIO4) | Linha de Dados I2C (Compartilhada) |
| | SCL | D1 (GPIO5) | Linha de Clock I2C (Compartilhada) |

> ⚠️ **Nota:** A maioria dos módulos comerciais SHT40 e displays OLED 0.91" já possui resistores de *pull-up* embutidos nas linhas I2C, dispensando o uso de componentes externos para essa montagem básica.

  <img width="1408" height="768" alt="image" src="https://github.com/user-attachments/assets/9461f459-1d0d-402f-893c-d2df9871e56d" />

