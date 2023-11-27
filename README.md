# NOTE~

## 吉祥物~
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
## c# 倒數計時器
```

public partial class Form1 : Form
    {
        System.Timers.Timer t;
        int h, m, s;
        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {
            t = new System.Timers.Timer();
            t.Interval = 1000;/// 間隔1000=1秒
            t.Elapsed += OnTimeEvent;
        }

        private void OnTimeEvent(object? sender, ElapsedEventArgs e)
        {
            Invoke(new Action(() => ///=>來接陳述塊 並用{}把事件包起來
            {
                s += 1;
                if(s==60)
                {
                    s = 0;
                    m += 1;
                }

                if(m==60)
                {
                    m = 0;
                    h += 1;
                }
                textBox1.Text=String.Format("{0}:{1}:{2}", h.ToString().PadLeft(2,'0'), m.ToString().PadLeft(2, '0'),s.ToString().PadLeft(2,'0'));///PadLeft代表要填充字符，代表希望最終長度是2字符'0'表示為指定填充的字符
            }));
            ///throw new NotImplementedException();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            t.Start();
        }

        private void button2_Click(object sender, EventArgs e)
        {
            t.Stop();
        }
  }
}
```







