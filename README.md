# NOTE~

## 興趣
梗圖!
## 圖片支援~
![皮卡啾] https://static.wixstatic.com/media/0fc723_4b961669e1a74fd8b64f194d90b6bcb2~mv2.gif



## c#陽春帳密登入介面
固定模式
```

 private void button1_Click(object sender, EventArgs e)
        {
            if(name.Text=="me" && pswd.Text=="12" )
            { 
                Form2 frame = new Form2();
                frame.ShowDialog();
           
            }

            else
            {
                Form3 frame = new Form3();
                frame.ShowDialog();


            }

        }

```
## c# BMI介面
兇版本
```

  private void button1_Click(object sender, EventArgs e)
        {
            double h, w,BMI;
            h = double.Parse(textBox1.Text)/100.0;
            w = double.Parse(textBox2.Text);

            BMI = w / (h * h);
            label3.Text = "計算出您的BMI為:" + BMI;


            if (BMI < 18.5)
                label4.Text = "體重太輕了,吃胖一點";
            if (BMI >= 18.5 && BMI <= 24.9)
                label4.Text = "正常,繼續保持下去";
            if (BMI >= 25 && BMI <= 29.9)
                label4.Text = "超重囉,最近是不是吃太好";
            if (BMI >= 30 && BMI <= 39.9)
                label4.Text = "肥胖警告,不要吃太多會被殺掉!";
            if (BMI > 40)
                label4.Text = "嚴重超標,人生重開吧";

       }
```

