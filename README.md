# 射擊對戰遊戲
# Authors:107321058, 106407023
# Input/Output Unit
。8x8 LED 矩陣，用來顯示對戰畫面。下圖為按下 clear 的初始畫面。
https://user-images.githubusercontent.com/38218129/72134911-283c4f80-33c0-11ea-8870-3dc2a66fd1e3.png
。LED 陣列，用來計玩家血量(左四事紅色玩家的，右四是綠色玩家的)。
https://user-images.githubusercontent.com/38218129/72135004-676aa080-33c0-11ea-8d8a-78c971f38bd7.png
# 功能說明:
綠色與紅色玩家對戰，打掉對方玩家血量則獲勝，同時沒血則平手。
# 程式模組說明:
module Shooting_Game(
output reg [7:0] R_color,//顯示紅色燈
output reg [7:0] G_color, //顯示綠色燈
output reg [7:0] B_color, //顯示藍色燈
output reg [3:0] column, //顯示燈亮的排
output reg [3:0] a_life, //A玩家生命
output reg [3:0] b_life,//B玩家生命
input a_up,a_down,a_left,a_right, //A玩家的移動(上下左右)
input b_up,b_down,b_left,b_right, //B玩家的移動(上下左右)
input MSB_in, CLK, Clear, //clear 初始值所有變數
input a_attack,a_defense, //A玩家的攻擊(a_attack)和防禦(a_defense)
input b_attack,b_defense//B玩家的攻擊(b_attack)和防禦(b_defense)
);
b_defense,b_attack,a_defense,a_attack-> 接到4-bit SW
MSB_in, Clear -> 接到PLUSE
a_up,a_down,a_left,a_right,b_up,b_down,b_left,b_right -> 接到8 DIPSW
R_color,G_color, B_color,column -> 接到8x8 LED 矩陣
a_life,b_life -> 接到LED 陣列
# Demo video:
https://drive.google.com/drive/u/0/folders/19mFnbH4ZPA-VfSv1K0sdk0MGnkvPGEr0
