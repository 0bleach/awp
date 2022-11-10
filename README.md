# A)Create an Console application that obtains four int values from the 
user and displays the product.

using System;<br />
using System.Collections.Generic;<br />
using System.Linq;<br />
using System.Text;
namespace ConsoleApplication1<br />
{
 class Program
 {
 static void Main(string[] args)
 {
 int num1, num2, num3, num4, prod;<br />
 Console.Write("Enter number 1: ");
 num1 = Int32.Parse(Console.ReadLine());
 Console.Write("Enter number 2: ");
 num2 = Convert.ToInt32(Console.ReadLine());
 Console.Write("Enter number 3: ");
 num3 = Convert.ToInt32(Console.ReadLine());
 Console.Write("Enter number 4: ");
 num4 = Convert.ToInt32(Console.ReadLine());
 prod = num1 * num2 * num3 * num4;
 Console.WriteLine(num1 + "*" + num2 + "*" + num3 + "*" + num4 + 
"=" + prod);
 Console.ReadKey();
 }
 }
}


# Create an application to demonstrate string operations.
using System;
namespace cmdLineArgs
{
class Program
{
static void Main(string[] args)
{
string str = args[0];
int n = Convert.ToInt32(args[1]);
Console.WriteLine("String:" + str);
Console.WriteLine("Number:" + n);
}
}
}

# Create an application that receives the (Student Id, Student 
Name, Course Name, Date of Birth) information from a set of 
students. The application should also display the information 
of all the students once the data entered.
using System;
namespace ArrayOfStructs
{
class Program
{
struct Student
{
public string studid, name, cname;
public int day, month, year;
}
static void Main(string[] args)
{
Student[] s = new Student[5];
int i;
for (i = 0; i < 5; i++)
{
Console.Write("Enter Student Id:");
s[i].studid = Console.ReadLine();
Console.Write("Enter Student name : ");
s[i].name = Console.ReadLine();
Console.Write("Enter Course name : ");
s[i].cname = Console.ReadLine();
Console.Write("Enter date of birth\n Enter day(1-31):");
s[i].day = Convert.ToInt32(Console.ReadLine());
Console.Write("Enter month(1-12):");
s[i].month = Convert.ToInt32(Console.ReadLine());
Console.Write("Enter year:");
s[i].year = Convert.ToInt32(Console.ReadLine());
}
https://E-next.in
TYIT ADVANCED WEB PROGRAMMING MANUAL
Khan S. Alam 5 https://E-next.in
Console.WriteLine("\n\nStudent's List\n");
for (i = 0; i < 5; i++)
{
Console.WriteLine("\nStudent ID : " + s[i].studid);
Console.WriteLine("\nStudent name : " + s[i].name);
Console.WriteLine("\nCourse name : " + s[i].cname);
Console.WriteLine("\nDate of birth(dd-mm-yy) : " + s[i].day + "-" + 
s[i].month +
"-" + s[i].year);
} } } }


# Create an application to demonstrate following operations
[i] Fibonacci Series
using System;
namespace ConsoleApplication3
{
class Program
{
static void Main(string[] args)
{
int num1=0,num2=1,num3,num4,num,counter;
Console.Write ("Upto how many number you want fibonacci series:");
num=int.Parse(Console.ReadLine());
counter=3;
Console.Write(num1+"\t"+num2);
while(counter<=num)
{
num3 = num1 + num2;
if (counter >= num)
break;
Console.Write("\t" + num3);
num1 = num2;
num2 = num3;
counter++;
}
}
}
}


#  Test for prime numbers.
CODE:
using System;
namespace testprime
{
class Program
{
static void Main(string[] args)
{
int num, counter;
Console.Write("Enter number:");
num = int.Parse(Console.ReadLine());
for (counter = 2; counter <= num / 2; counter++)
{
if ((num % counter) == 0)
break;
}
if (num == 1)
Console.WriteLine(num + "is neither prime nor composite");
else if(counter<(num/2))
Console.WriteLine(num+"is not prime number");
else
Console.WriteLine(num+"is prime number");
}
}



# ] Test for prime numbers.
CODE:
using System;
namespace testprime
{
class Program
{
static void Main(string[] args)
{
int num, counter;
Console.Write("Enter number:");
num = int.Parse(Console.ReadLine());
for (counter = 2; counter <= num / 2; counter++)
{
if ((num % counter) == 0)
https://E-next.in
TYIT ADVANCED WEB PROGRAMMING MANUAL
Khan S. Alam 10 https://E-next.in
break;
}
if (num == 1)
Console.WriteLine(num + "is neither prime nor composite");
else if(counter<(num/2))
Console.WriteLine(num+"is not prime number");
else
Console.WriteLine(num+"is prime number");
}
}
Program.cs
using System;
namespace TrafficDelegateExample
{
class Program
{
static void Main(string[] args)
{
TrafficSignal ts = new TrafficSignal();
ts.IdentifySignal();
ts.display();
} } }


# Create a Web Form to demonstrate the use of User Controls.
WebUserControl1.ascx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
namespace guest{
public partial class WebUserControl1 : System.Web.UI.UserControl{
protected void Page_Load(object sender, EventArgs e){
}
protected void Button1_Click(object sender, EventArgs e){
TextBox2.Text = " Welcome " + TextBox1.Text;
}
}
}
WebForm1.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
namespace guest{
public partial class WebForm1 : System.Web.UI.Page{
protected void Page_Load(object sender, EventArgs e)
{
}
protected void Button1_Click(object sender, EventArgs e){
TextBox2.Text = "Hello Guest " + TextBox1.Text;
}
}
}


# Create a web application bind data in a multiline textbox by querying in another 
textbox.
Source Code:
WebForm1.aspx
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs"
Inherits="p6a.WebForm1" %>
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
<title></title>
</head>
<body>
<form id="form1" runat="server">
<div>
<asp:TextBox ID="TextBox1" runat="server"></asp:TextBox>&nbsp;
<asp:TextBox ID="TextBox2" runat="server" TextMode="MultiLine"></asp:TextBox>
<br />
<br />
<asp:Button ID="Button1" runat="server" OnClick="Button1_Click" Text="Button" />
<br />
<br />
<asp:SqlDataSource ID="SqlDataSource11" runat="server" ConnectionString="<%$
ConnectionStrings:employeeConnectionString %>" SelectCommand="SELECT * FROM
[Student]"></asp:SqlDataSource>
<br />
</div>
</form>
</body>
</html>
WebForm1.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;
namespace prac6a
{
public partial class WebForm1 : System.Web.UI.Page
{
SqlConnection cn = new SqlConnection(@"Data Source=LAPTOP-LUI6BQOQ\sqlexpress;Initial
Catalog=employee;Integrated Security=True;Pooling=False");
SqlCommand co = new SqlCommand();
SqlDataReader ds;
protected void Page_Load(object sender, EventArgs e)
{
cn.Open(); co.Connection
= cn;
}
protected void Button1_Click(object sender, EventArgs e)
{
co.CommandText = "Select * from Student where name='" + TextBox1.Text + "';";ds = 
co.ExecuteReader();
while(ds.Read())
{
TextBox2.Text += ds[0].ToString() + "\t" + ds[1].ToString() + "\n";
}
cn.Close();
}
}
}


#Demonstrate the use of Data list link control.
Source Code:
WebForm1.aspx
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs"
Inherits="p6c.WebForm1" %>
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
<title></title>
</head>
<body>
<form id="form1" runat="server">
<div>
<asp:SqlDataSource ID="SqlDataSource1" runat="server" ConnectionString="<%$
ConnectionStrings:employeeConnectionString %>" SelectCommand="SELECT * FROM
[Student]"></asp:SqlDataSource>
<br />
<br />
<asp:DataList ID="DataList1" runat="server" DataKeyField="Id" DataSourceID="SqlDataSource1">
<ItemTemplate>
Id:
<asp:Label ID="IdLabel" runat="server" Text='<%# Eval("Id") %>' />
<br />
name:
<asp:Label ID="nameLabel" runat="server" Text='<%# Eval("name") %>' />
<br /><br />
</ItemTemplate>
</asp:DataList>
</div>
</form>
</body>
</html>

# Create a web application to display Databinding using dropdownlist control.
Source Code:
WebForm1.aspx
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs"
Inherits="practical7a.WebForm1" %>
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
<title></title>
</head>
<body>
<form id="form1" runat="server">
<div>
<asp:TextBox ID="TextBox1" runat="server"></asp:TextBox>
&nbsp;&nbsp;&nbsp;
<asp:Button ID="Button1" runat="server" OnClick="Button1_Click" Text="Button" />
&nbsp;
&nbsp;
<asp:Label ID="Label1" runat="server" Text="Label"></asp:Label>
<asp:DropDownList ID="DropDownList1" runat="server"
OnSelectedIndexChanged="DropDownList1_SelectedIndexChanged">
</asp:DropDownList>
<br />
<br />
<asp:SqlDataSource ID="SqlDataSource1" runat="server" ConnectionString="<%$
ConnectionStrings:employeeConnectionString %>" SelectCommand="SELECT * FROM
[Student]"></asp:SqlDataSource> </div>
</form>
</body>
</html>
WebForm1.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;
namespace practical7a
{
public partial class WebForm1 : System.Web.UI.Page
{
SqlConnection sqlcon = new SqlConnection(@"Data Source= LAPTOP-LUI6BQOQ\sqlexpress;Initial
Catalog=employee;Integrated Security=True; Pooling=False ");
protected void Page_Load(object sender, EventArgs e)
{
if (IsPostBack == false)
{
sqlcon.Open();
SqlCommand cmd = new SqlCommand("select * from Student", sqlcon);
SqlDataReader reader = cmd.ExecuteReader(); DropDownList1.DataSource =
reader;
DropDownList1.DataTextField = "Name";
DropDownList1.DataBind(); reader.Close();
sqlcon.Close();
}
}
protected void Button1_Click(object sender, EventArgs e)
{
Label1.Text = "You are Selected:" + DropDownList1.SelectedValue;
}
protected void DropDownList1_SelectedIndexChanged(object sender, EventArgs e)
{
TextBox1.Text = DropDownList1.Text;
}
}
}


# Create a web application for inserting and deleting record from a database(Using 
Execute-Non Query).
Source Code:
WebForm1.aspx
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs"
Inherits="practical7c.WebForm1" %>
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
<title></title>
</head>
<body>
<form id="form1" runat="server">
<div>
<asp:TextBox ID="TextBox1" runat="server"></asp:TextBox> &nbsp;
<asp:TextBox ID="TextBox2" runat="server"></asp:TextBox> &nbsp;
<asp:TextBox ID="TextBox3" runat="server"></asp:TextBox> &nbsp;
<asp:TextBox ID="TextBox4" runat="server"></asp:TextBox><br /><br />
<asp:Button ID="Button1" runat="server" OnClick="Button1_Click" Text="Insert" /> &nbsp;
<asp:Button ID="Button2" runat="server" OnClick="Button2_Click" Text="Delete" /> &nbsp;
<asp:Button ID="Button3" runat="server" OnClick="Button3_Click" Text="View" /><br /><br />
<asp:GridView ID="GridView1" runat="server" AutoGenerateColumns="False"
DataKeyNames="Sno" DataSourceID="SqlDataSource1">
<Columns>
<asp:BoundField DataField="Sno" HeaderText="Sno" ReadOnly="True" SortExpression="Sno" />
<asp:BoundField DataField="Name" HeaderText="Name" SortExpression="Name" />
<asp:BoundField DataField="City" HeaderText="City" SortExpression="City" />
<asp:BoundField DataField="Class" HeaderText="Class" SortExpression="Class" />
</Columns>
</asp:GridView>
<br />
<asp:SqlDataSource ID="SqlDataSource1" runat="server" ConnectionString="<%$
ConnectionStrings:BookConnectionString2 %>" SelectCommand="SELECT * FROM
[bk]"></asp:SqlDataSource>
</div>
</form>
</body>
</html>
WebForm1.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;
namespace p7c
{
public partial class WebForm1 : System.Web.UI.Page
{
SqlConnection cn = new SqlConnection(@"Data Source=LAPTOP-LUI6BQOQ\sqlexpress;Initial
Catalog=Book;Integrated Security=True;Pooling=False");
SqlCommand co = new SqlCommand();
SqlDataReader ds;
SqlParameter @p1, @p2, @p3, @p4;
protected void Page_Load(object sender, EventArgs e)
{
cn.Open(); co.Connection
= cn;
}
protected void Button1_Click(object sender, EventArgs e)
{
@p1 = new SqlParameter();
@p1.ParameterName = "Sno";
@p1.SqlDbType = System.Data.SqlDbType.Int;
@p2 = new SqlParameter(); @p2.ParameterName =
"Name";
@p2.SqlDbType = System.Data.SqlDbType.VarChar;@p3
= new SqlParameter();
@p3.ParameterName = "Class";
@p3.SqlDbType = System.Data.SqlDbType.VarChar;@p4
= new SqlParameter();
@p4.ParameterName = "City";
@p4.SqlDbType = System.Data.SqlDbType.VarChar;
co.Parameters.AddWithValue("@p1", TextBox1.Text);
co.Parameters.AddWithValue("@p2", TextBox2.Text);
co.Parameters.AddWithValue("@p3", TextBox3.Text);
co.Parameters.AddWithValue("@p4", TextBox4.Text);
co.CommandText = "insert into bk(Sno,Name,Class,City) values(@p1,@p2,@p3,@p4);";
co.ExecuteNonQuery();
}
protected void Button2_Click(object sender, EventArgs e)
{
String InsertQuery = "delete from bk where Sno=@p1";
SqlCommand cmd = new SqlCommand(InsertQuery, cn);
cmd.Parameters.AddWithValue("@p1", TextBox1.Text);
cmd.ExecuteNonQuery();
cn.Close();
}
protected void Button3_Click(object sender, EventArgs e)
{
co.CommandText = "select * from bk;";ds = 
co.ExecuteReader(); GridView1.DataBind();
}
}
}


# : Create a web application to demonstrate reading and writing operation with XML.
Source Code:
WebForm1.aspx
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs"
Inherits="Prac10A.WebForm1" %>
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
<title></title>
</head>
<body>
<form id="form1" runat="server">
<div>
<asp:Button ID="Button1" runat="server" OnClick="Button1_Click" style="height: 26px" Text="ReadXML" />
<br />
<br />
<asp:GridView ID="GridView1" runat="server" AutoGenerateColumns="False">
<Columns>
<asp:BoundField DataField="name" HeaderText="Name" />
<asp:BoundField DataField="roll" HeaderText="Roll Number" />
</Columns>
</asp:GridView>
<br />
<br />
<asp:Button ID="Button2" runat="server" OnClick="Button2_Click" Text="Write XML" />
</div>
</form>
</body>
</html>
WebForm1.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data;
using System.Xml;
namespace Prac10A{
public partial class WebForm1 : System.Web.UI.Page {
protected void Page_Load(object sender, EventArgs e) {
}
protected void Button1_Click(object sender, EventArgs e)
{
DataSet ds = new DataSet();
ds.ReadXml(Server.MapPath("XMLFile1.xml"));
GridView1.DataSource = ds.Tables[0].DefaultView;
GridView1.DataBind();
}
protected void Button2_Click(object sender, EventArgs e)
{
XmlWriterSettings set = new XmlWriterSettings();
set.Indent = true;
using (XmlWriter xmlW =
XmlWriter.Create(@"C:\AWP\Practicals\Prac10A\Prac10A\XMLFile2.xml", set))
{
xmlW.WriteStartElement("Student");
xmlW.WriteElementString("Name","XYZ");
xmlW.WriteElementString("Class","TYIT");
xmlW.WriteEndElement();
}
Response.Write("Okay!");
}
}
}
XMLFile1.xml
<?xml version="1.0" encoding="utf-8" ?>
<student>
<name>abc</name>
<roll>1</roll>
</student>


# : Create a web application to demonstrate use of various Ajax control.
Source Code:
WebForm1.aspx
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs"
Inherits="Prac10c.WebForm1" %>
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
</head>
<body>
<form id="form1" runat="server">
<div>
<asp:ScriptManager ID="ScriptManager1" runat="server">
</asp:ScriptManager><br />
<asp:Button ID="Button1" runat="server" OnClick="Button1_Click" Text="Show Time" /><br /><br />
<asp:TextBox ID="TextBox1" runat="server"></asp:TextBox> <br />
<asp:UpdateProgress ID="UpdateProgress1" runat="server">
<ProgressTemplate> Please wait for some time</ProgressTemplate>
</asp:UpdateProgress<br > <br /> <br />
<asp:UpdatePanel ID="UpdatePanel1" runat="server"> </asp:UpdatePanel>
</div>
</form>
</body>
</html>
WebForm1.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
namespace Prac10c{
public partial class WebForm1 : System.Web.UI.Page{
protected void Page_Load(object sender, EventArgs e){
System.Threading.Thread.Sleep(2000);
}
protected void Button1_Click(object sender, EventArgs e){
TextBox1.Text = DateTime.Now.ToLongTimeString();
}
}
}


# Programs to create and use DLL
Date- 01/10/2022
Source Code:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
namespace Prac_11
{
class Program
{
static void Main(string[] args)
{
Prac11.Class1 c = new Prac11.Class1();int 
t = c.add(20, 40);
Console.WriteLine("Addition={0}", t);
Console.ReadKey();
}
}
}
Class1.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
namespace Prac11
{
public class Class1
{
public int add(int a, int b)
{
int c = a + b;
return c;
}
}
}
WebUserControl1.ascx
<%@ Control Language="C#" AutoEventWireup="true" CodeBehind="WebUserControl1.ascx.cs"
Inherits="guest.WebUserControl1" %>
<asp:TextBox ID="TextBox1" runat="server"></asp:TextBox>
<asp:Button ID="Button1" runat="server" OnClick="Button1_Click" Text="Button" />
<asp:TextBox ID="TextBox2" runat="server"></asp:TextBox>
WebForm1.aspx
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs"
Inherits="guest.WebForm1" %>
<%@Register Src="~/WebUserControl1.ascx" TagName="WebUserControl" TagPrefix="uc1" %>
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
<title></title>
</head>
<body>
<form id="form1" runat="server">
<div>
<asp:TextBox ID="TextBox1" runat="server"></asp:TextBox>
<asp:Button ID="Button1" runat="server" OnClick="Button1_Click" style="height: 26px"
Text="Button" />
<asp:TextBox ID="TextBox2" runat="server"></asp:TextBox>
<br />
<uc1:WebUserControl runat="server" ID="WebUserControl1" />
</div>
</form>
</body>
</html>

