
import java.awt.Font;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.util.Set;
import javax.swing.*;

public class CalculatorGUI implements ActionListener {

    JFrame frame;
    JLabel lblNumber1, lblNumber2, lblResult;
    JTextField jtfNumber1, jtfNumber2, jtfResult;
    JButton add, sub, mul, div;

    CalculatorGUI() {
        frame = new JFrame("Tinh Toan");
        Font font = new Font("Arial", Font.BOLD, 20);
        frame.setSize(500, 500);

        lblNumber1 = new JLabel("First number");
        lblNumber2 = new JLabel("Second number");
        lblResult = new JLabel("Result ");

        lblNumber1.setBounds(50, 50, 200, 30);
        lblNumber2.setBounds(50, 100, 200, 30);
        lblResult.setBounds(50, 220, 200, 30);
        
        lblNumber1.setFont(font);
        lblNumber2.setFont(font);
        lblResult.setFont(font);

        jtfNumber1 = new JTextField();
        jtfNumber2 = new JTextField();
        jtfResult = new JTextField();

        jtfNumber1.setBounds(220, 50, 200, 30);
        jtfNumber2.setBounds(220, 100, 200, 30);
        jtfResult.setBounds(220, 220, 200, 30);

        add = new JButton("+");
        sub = new JButton("-");
        mul = new JButton("*");
        div = new JButton("/");

        add.addActionListener(this);
        sub.addActionListener(this);
        mul.addActionListener(this);
        div.addActionListener(this);

        add.setBounds(80, 160, 70, 40);
        sub.setBounds(160, 160, 70, 40);
        mul.setBounds(240, 160, 70, 40);
        div.setBounds(320, 160, 70, 40);

        frame.add(lblNumber1);
        frame.add(lblNumber2);
        frame.add(lblResult);
        frame.add(jtfNumber1);
        frame.add(jtfNumber2);
        frame.add(jtfResult);
        frame.add(add);
        frame.add(sub);
        frame.add(mul);
        frame.add(div);

        frame.setLocationRelativeTo(null);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setLayout(null);
        frame.setVisible(true);
    }

    @Override
    public void actionPerformed(ActionEvent ae) {
        try {
            double firstNumber = Double.parseDouble(jtfNumber1.getText());
            double secondNumber = Double.parseDouble(jtfNumber2.getText());
            if (ae.getSource() == add) {
                jtfResult.setText(firstNumber + secondNumber + "");
            } else if (ae.getSource() == sub) {
                jtfResult.setText(firstNumber - secondNumber + "");
            } else if (ae.getSource() == mul) {
                jtfResult.setText(firstNumber * secondNumber + "");
            } else {
                if (secondNumber == 0) {
                    throw new IllegalArgumentException("Cannot divide by zero!");
                } else {
                    jtfResult.setText(firstNumber / secondNumber + "");
                }
            }
        } catch (NumberFormatException e) {
            JOptionPane.showMessageDialog(null, "Please enter valid numbers!");
        } catch (IllegalArgumentException e) {
            JOptionPane.showMessageDialog(null, e.getMessage());
        }
    }

    public static void main(String[] args) {
        new CalculatorGUI();
    }
}
