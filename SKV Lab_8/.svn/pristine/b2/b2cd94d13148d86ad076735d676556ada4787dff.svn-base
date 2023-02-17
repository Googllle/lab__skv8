Imports System.Windows.Forms.VisualStyles.VisualStyleElement
Imports System.Math
Imports System.Buffers
Imports System.Windows.Forms.Design.AxImporter

Public Class Form1
    Dim a, b, h, simp, n, P As Double

    Private Sub Button1_Click(sender As Object, e As EventArgs) Handles Button1.Click
        a = Val(TextBox1.Text)
        b = Val(TextBox2.Text)
        h = 0.1
        n = (b - a) / h
        simp = ((b - a) / 6) * (f(a) + 4 * f((a + b) / 2) + f(b))
        TextBox4.Text = simp
    End Sub
    Function f(x) As Single
        'Сама функция
        f = x * Log(x)
    End Function
    Private Sub Button2_Click(sender As Object, e As EventArgs) Handles Button2.Click
        Dim S1, S2 As Double
        a = Val(TextBox1.Text)
        b = Val(TextBox2.Text)
        h = 0.1
        n = (b - a) / h
        S1 = 0
        For i = 1 To n - 1
            S1 = S1 + f(h * i + a)
        Next i
        S2 = 0
        For i = 1 To n
            S2 = S2 + f(h * i - 0.5 * h + a)
        Next i
        'Итоговая формула
        P = h / 3 * (0.5 * f(a) + S1 + 2 * S2 + 0.5 * f(b))
        TextBox5.Text = P
    End Sub

End Class

