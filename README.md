namespace WindowsFormsApp1
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void label1_Click(object sender, EventArgs e)
        {

        }

        private void button1_Click(object sender, EventArgs e)
        {
            //Создаем объект формы 2
            Form2 form2 = new Form2();
            //Передаем данные через свойство
            form2.Label = textBox1.Text;
            //Показываем форму
            form2.Show();
            //Если надо показать как диалог, то надо написать так
            // form2.ShowDialog();
            // Скрываем форму 1
            this.Hide();
        }

        private void Form1_Load(object sender, EventArgs e)
        {

        }
    }
}




namespace WindowsFormsApp1
{
    public partial class Form2 : Form
    {
        public Form2()
        {
            InitializeComponent();
            Form1 form1 = new Form1();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            //Создаем объект формы 1
            Form1 form1 = new Form1();
            //Показываем форму 1
            form1.Show();
            // Закрываем форму 2
            this.Close();
        }

        private void label1_Click(object sender, EventArgs e)
        {

        }
        public string Label
        {
            get { return label1.Text; }
            set { label1.Text = value; }
        }

        private void button2_Click(object sender, EventArgs e)
        {
            Application.Exit();
        }
    }

}

