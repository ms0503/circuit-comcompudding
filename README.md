ComComPudding
=============

ComComPuddingは「通信」を主軸に設計された汎用基板です。
MCUはSTM32F405RGT6を採用しコンパクトながら素早く処理することができます。

# 使用IC
## MCP2542WFD
高速通信可能なCANトランシーバです。
詳細は[データシート](https://ww1.microchip.com/downloads/aemDocuments/documents/APID/ProductDocuments/DataSheets/MCP2542FD-MCP2542WFD-4WFD-Data-Sheet-DS20005514C.pdf)
をご覧下さい。

## STM32F405RGT6
メインの処理を担当するMCUです。
詳細は[データシート](https://www.st.com/resource/en/datasheet/stm32f405rg.pdf)
及び[リファレンスマニュアル](https://www.stmcu.jp/download/?dlid=51544_jp)
をご覧下さい。

# インターフェース
## CAN
CAN(Control Area Network)向けのポートが1系統、2つ搭載されており、CANへのアクセス、
5V電源の供給を行うことが出来ます。
### 信号レベル
- マイコン側：3.3V
- 端子側：5V

### マイコンピン
TX：PA11
RX：PA12

## I²C
I²C(Inter-Intergrated Circuit)向けのポートが1系統、1つ搭載されており、I²Cへのアクセス、
5V電源の供給を行うことが出来ます。
### 信号レベル
3.3V
### マイコンピン
I2C1\_SCL：PB6
I2C1\_SDA：PB7

## LED
基板表面に実装された4つのLEDで簡易的な状態表示を行うことが出来ます。
### 信号レベル
3.3V
### マイコンピン
LED1：PB12
LED2：PB13
LED3：PB14
LED4：PB15

## SPI
SPI(Serial Peripheral Interface)向けのポートが2系統、3つ搭載されており、SlaveとしてのMasterとの通信、
MasterとしてのSlave(最大2台まで)との通信、5V電源の供給を行うことが出来ます。  
SPI1をSlave動作、SPI2をMaster動作とすることを想定しています。
### 信号レベル
3.3V
### マイコンピン
SPI1\_SCK：PA5
SPI1\_MISO：PA6
SPI1\_MOSI：PA7
SPI1\_SS：PA4
SPI2\_SCK：PB10
SPI2\_MISO：PC2
SPI2\_MOSI：PC3
SPI2\_SS\_1：PC0
SPI2\_SS\_2：PC1

## U(S)ART
USART(Universal Synchronous-Asynchronous Receiver and Transmitter)向けのポートが4つ、
UART(Universal Asynchronous Receiver and Transmitter)向けのポートが2つ、計6つ搭載されており、
U(S)ARTデバイスとの通信、5V電源の供給を行うことが出来ます。
### 信号レベル
3.3V
### マイコンピン
USART1\_TX：PA9
USART1\_RX：PA10
USART2\_TX：PA2
USART2\_RX：PA3
USART3\_TX：PC10
USART3\_RX：PB11
UART4\_TX：PA0
UART4\_RX：PA1
UART5\_TX：PC12
UART5\_RX：PD2
USART6\_TX：PC6
USART6\_RX：PC7

# ライブラリ
この基板は一部のシンボル・フットプリントに[kicad-mecha](https://github.com/ms0503/kicad-mecha.git)を使用しています。
別途インポートした上でご利用下さい。

# 設計者
Sora Tonami <[ms0503@outlook.com](mailto:ms0503@outlook.com)>

# ライセンス
この基板のデータは[MITライセンス](LICENSE.md)の下に公開されます。ご自由に改変・再配布して頂いて構いません。

