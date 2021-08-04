# First-Project
Very simple Hello World project
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Tamrin_1
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void lblenteryourname_MouseHover(object sender, EventArgs e)
        {
          
        }

        private void lblenteryourname_MouseMove(object sender, MouseEventArgs e)
        {
            lblenteryourname.ForeColor = Color.Red;
        }

        private void lblenteryourname_MouseLeave(object sender, EventArgs e)
        {
            lblenteryourname.ForeColor = Color.Black;
        }

        private void btnsayhello_Click(object sender, EventArgs e)
        {
            string s;
            s = "Hello " + txttextbox.Text;
            lblResult.Text = s ;
        }

        private void btnclear_Click(object sender, EventArgs e)
        {
            txttextbox.Text = "";
            lblResult.Text = "";
            btnsayhello.Focus();
        }

        private void txttextbox_TextChanged(object sender, EventArgs e)
        {
            if  (txttextbox.Text == "") 
               btnsayhello.Enabled = false;
            else
              btnsayhello.Enabled=  true;
            btnclear.Enabled = Convert.ToBoolean(txttextbox.Text.Length);
        }

        private void Form1_Load(object sender, EventArgs e)
        {
            txttextbox_TextChanged(null, null);
        }

        private void btnexit_Click(object sender, EventArgs e)
        {
            Application.Exit(); 
        }
    }
}
