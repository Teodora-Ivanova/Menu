# Menu
package finalProject;

import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JLabel;
import java.awt.Font;
import java.awt.Color;
import java.awt.Component;

import javax.swing.SwingConstants;
import javax.swing.JPanel;
import javax.swing.border.TitledBorder;
import javax.swing.border.BevelBorder;
import javax.swing.border.LineBorder;
import javax.swing.border.MatteBorder;
import javax.swing.UIManager;
import java.awt.BorderLayout;
import com.jgoodies.forms.layout.FormLayout;
import com.jgoodies.forms.layout.ColumnSpec;
import com.jgoodies.forms.layout.RowSpec;
import javax.swing.BoxLayout;
import javax.swing.JSplitPane;
import javax.swing.JComboBox;
import javax.swing.DefaultComboBoxModel;
import javax.swing.JButton;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;
import javax.swing.JTextField;

public class Menu {

	private JFrame frame;
	private JTextField quantitySalads;
	private JTextField quantitySoups;
	private JTextField quantityMainCourses;
	private JTextField quantityDesserts;
	private JTextField quantityHotDrinks;
	private JTextField quantityUncarbDrinks;
	private JTextField quantityCarbDrinks;
	private JTextField quantityAlcDrinks;
	private JTextField txtFieldCostOfMeal;
	private JTextField txtFieldCostOfDrinks;
	private JTextField txtFieldTotal;
	private JTextField txtReceipt;
	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					Menu window = new Menu();
					window.frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	/**
	 * Create the application.
	 */
	public Menu() {
		initialize();
	}
	
	

	private void initialize() {
		frame = new JFrame();
		frame.setBounds(0, 0, 1400, 700);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.getContentPane().setLayout(null);

		JLabel labelMenu = new JLabel("Menu");
		labelMenu.setHorizontalAlignment(SwingConstants.CENTER);
		labelMenu.setForeground(new Color(0, 0, 0));
		labelMenu.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 85));
		labelMenu.setBounds(433, 0, 802, 87);
		frame.getContentPane().add(labelMenu);

		JPanel foodPanel = new JPanel();
		foodPanel.setBorder(new LineBorder(new Color(0, 0, 0), 5, true));
		foodPanel.setBounds(40, 103, 500, 255);
		frame.getContentPane().add(foodPanel);
		foodPanel.setLayout(null);

		JLabel labelFood = new JLabel("Food");
		labelFood.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 40));
		labelFood.setHorizontalAlignment(SwingConstants.CENTER);
		labelFood.setForeground(new Color(0, 0, 0));
		labelFood.setBounds(10, 11, 480, 35);
		foodPanel.add(labelFood);

		JComboBox saladsBox = new JComboBox();
		saladsBox.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 20));
		saladsBox.setModel(new DefaultComboBoxModel(
				new String[] { "Salads", "Shopska salad", "Shepherd's salad", "Mixed salad" }));
		saladsBox.setBounds(51, 61, 198, 32);
		foodPanel.add(saladsBox);

		JComboBox soupsBox = new JComboBox();
		soupsBox.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 20));
		soupsBox.setModel(
				new DefaultComboBoxModel(new String[] { "Soups", "Chicken soup", "Meatball soup", "Vegetable soup" }));
		soupsBox.setBounds(51, 104, 198, 32);
		foodPanel.add(soupsBox);

		JComboBox mainCoursesBox = new JComboBox();
		mainCoursesBox.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 20));
		mainCoursesBox.setModel(new DefaultComboBoxModel(
				new String[] { "Main courses", "Chicken with potatoes", "Rice with vegetables", "Spaghetti " }));
		mainCoursesBox.setBounds(51, 147, 198, 32);
		foodPanel.add(mainCoursesBox);

		JComboBox dessertsBox = new JComboBox();
		dessertsBox.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 20));
		dessertsBox
				.setModel(new DefaultComboBoxModel(new String[] { "Desserts", "Ice cream", "Pancake", "Pumpkin pie" }));
		dessertsBox.setBounds(51, 190, 198, 32);
		foodPanel.add(dessertsBox);

		JLabel lblDessertsQuantity = new JLabel("Quantity:");
		lblDessertsQuantity.setForeground(new Color(255, 0, 0));
		lblDessertsQuantity.setHorizontalAlignment(SwingConstants.CENTER);
		lblDessertsQuantity.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 15));
		lblDessertsQuantity.setBounds(273, 193, 70, 29);
		foodPanel.add(lblDessertsQuantity);

		JLabel lblMainCoursesQuantity = new JLabel("Quantity:");
		lblMainCoursesQuantity.setForeground(new Color(255, 0, 0));
		lblMainCoursesQuantity.setHorizontalAlignment(SwingConstants.CENTER);
		lblMainCoursesQuantity.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 15));
		lblMainCoursesQuantity.setBounds(273, 147, 70, 29);
		foodPanel.add(lblMainCoursesQuantity);

		JLabel lblSoupsQuantity = new JLabel("Quantity:");
		lblSoupsQuantity.setForeground(new Color(255, 0, 0));
		lblSoupsQuantity.setHorizontalAlignment(SwingConstants.CENTER);
		lblSoupsQuantity.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 15));
		lblSoupsQuantity.setBounds(273, 107, 70, 29);
		foodPanel.add(lblSoupsQuantity);

		JLabel lblSaladsQuantity = new JLabel("Quantity:");
		lblSaladsQuantity.setForeground(new Color(255, 0, 0));
		lblSaladsQuantity.setHorizontalAlignment(SwingConstants.CENTER);
		lblSaladsQuantity.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 15));
		lblSaladsQuantity.setBounds(273, 64, 70, 29);
		foodPanel.add(lblSaladsQuantity);

		quantitySalads = new JTextField();
		quantitySalads.setBounds(353, 61, 105, 32);
		foodPanel.add(quantitySalads);
		quantitySalads.setColumns(10);

		quantitySoups = new JTextField();
		quantitySoups.setColumns(10);
		quantitySoups.setBounds(353, 104, 105, 32);
		foodPanel.add(quantitySoups);

		quantityMainCourses = new JTextField();
		quantityMainCourses.setColumns(10);
		quantityMainCourses.setBounds(353, 147, 105, 32);
		foodPanel.add(quantityMainCourses);

		quantityDesserts = new JTextField();
		quantityDesserts.setColumns(10);
		quantityDesserts.setBounds(353, 191, 105, 32);
		foodPanel.add(quantityDesserts);

		JPanel drinksPanel = new JPanel();
		drinksPanel.setBorder(new LineBorder(new Color(0, 0, 0), 5, true));
		drinksPanel.setBounds(40, 390, 500, 247);
		frame.getContentPane().add(drinksPanel);
		drinksPanel.setLayout(null);

		JLabel labelDrinks = new JLabel("Drinks");
		labelDrinks.setForeground(new Color(0, 0, 0));
		labelDrinks.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 40));
		labelDrinks.setHorizontalAlignment(SwingConstants.CENTER);
		labelDrinks.setBounds(10, 11, 480, 38);
		drinksPanel.add(labelDrinks);

		JComboBox hotDrinksBox = new JComboBox();
		hotDrinksBox.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 20));
		hotDrinksBox.setModel(new DefaultComboBoxModel(
				new String[] { "Hot drinks", "Coffee", "Hot chocolate", "Cappuccino", "Latte", "Milk" }));
		hotDrinksBox.setBounds(51, 57, 197, 32);
		drinksPanel.add(hotDrinksBox);

		JComboBox uncarbonatedDrinksBox = new JComboBox();
		uncarbonatedDrinksBox.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 18));
		uncarbonatedDrinksBox.setModel(new DefaultComboBoxModel(new String[] { "Uncarbonated drinks", "Water",
				"Orange juice", "Apple juice", "Banana juice", "Peach juice", "Appricot juice", "" }));
		uncarbonatedDrinksBox.setBounds(51, 100, 197, 38);
		drinksPanel.add(uncarbonatedDrinksBox);

		JComboBox carbonatedDrinksBox = new JComboBox();
		carbonatedDrinksBox.setModel(new DefaultComboBoxModel(
				new String[] { "Carbonated drinks", "Coca Cola", "Fanta", "Sprite", "Tonic" }));
		carbonatedDrinksBox.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 17));
		carbonatedDrinksBox.setBounds(51, 149, 197, 32);
		drinksPanel.add(carbonatedDrinksBox);

		JComboBox alcoholDrinksBox = new JComboBox();
		alcoholDrinksBox.setModel(new DefaultComboBoxModel(
				new String[] { "Alcohol drinks", "Whiskey", "Vodka", "Red wine", "White wine", "Gin" }));
		alcoholDrinksBox.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 20));
		alcoholDrinksBox.setBounds(51, 192, 197, 32);
		drinksPanel.add(alcoholDrinksBox);

		JLabel lblHotDrinksQuantity = new JLabel("Quantity:");
		lblHotDrinksQuantity.setForeground(new Color(255, 0, 0));
		lblHotDrinksQuantity.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 15));
		lblHotDrinksQuantity.setHorizontalAlignment(SwingConstants.CENTER);
		lblHotDrinksQuantity.setBounds(276, 60, 70, 29);
		drinksPanel.add(lblHotDrinksQuantity);

		JLabel lblUncarbDrinksQuantity = new JLabel("Quantity:");
		lblUncarbDrinksQuantity.setForeground(new Color(255, 0, 0));
		lblUncarbDrinksQuantity.setHorizontalAlignment(SwingConstants.CENTER);
		lblUncarbDrinksQuantity.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 15));
		lblUncarbDrinksQuantity.setBounds(276, 105, 70, 29);
		drinksPanel.add(lblUncarbDrinksQuantity);

		JLabel lblCarbDrinksQuantity = new JLabel("Quantity:");
		lblCarbDrinksQuantity.setForeground(new Color(255, 0, 0));
		lblCarbDrinksQuantity.setHorizontalAlignment(SwingConstants.CENTER);
		lblCarbDrinksQuantity.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 15));
		lblCarbDrinksQuantity.setBounds(276, 151, 70, 29);
		drinksPanel.add(lblCarbDrinksQuantity);

		JLabel lblAlcDrinksQuantity = new JLabel("Quantity:");
		lblAlcDrinksQuantity.setForeground(new Color(255, 0, 0));
		lblAlcDrinksQuantity.setHorizontalAlignment(SwingConstants.CENTER);
		lblAlcDrinksQuantity.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 15));
		lblAlcDrinksQuantity.setBounds(276, 195, 70, 29);
		drinksPanel.add(lblAlcDrinksQuantity);

		quantityHotDrinks = new JTextField();
		quantityHotDrinks.setColumns(10);
		quantityHotDrinks.setBounds(356, 57, 105, 32);
		drinksPanel.add(quantityHotDrinks);

		quantityUncarbDrinks = new JTextField();
		quantityUncarbDrinks.setColumns(10);
		quantityUncarbDrinks.setBounds(356, 100, 105, 32);
		drinksPanel.add(quantityUncarbDrinks);

		quantityCarbDrinks = new JTextField();
		quantityCarbDrinks.setColumns(10);
		quantityCarbDrinks.setBounds(356, 149, 105, 32);
		drinksPanel.add(quantityCarbDrinks);

		quantityAlcDrinks = new JTextField();
		quantityAlcDrinks.setColumns(10);
		quantityAlcDrinks.setBounds(356, 192, 105, 32);
		drinksPanel.add(quantityAlcDrinks);

		JPanel panel = new JPanel();
		panel.setBorder(new LineBorder(new Color(0, 0, 0), 5, true));
		panel.setBounds(626, 103, 303, 534);
		frame.getContentPane().add(panel);
		panel.setLayout(null);

		JLabel lblCostOfMeal = new JLabel("Cost of the meal:");
		lblCostOfMeal.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 17));
		lblCostOfMeal.setBounds(15, 238, 141, 28);
		panel.add(lblCostOfMeal);

		txtFieldCostOfMeal = new JTextField();
		txtFieldCostOfMeal.setBounds(166, 238, 98, 28);
		panel.add(txtFieldCostOfMeal);
		txtFieldCostOfMeal.setColumns(10);
		
		JLabel lblCostOfDrinks = new JLabel("Cost of the drinks:");
		lblCostOfDrinks.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 17));
		lblCostOfDrinks.setBounds(15, 153, 141, 28);
		panel.add(lblCostOfDrinks);
		
		txtFieldCostOfDrinks = new JTextField();
		txtFieldCostOfDrinks.setBounds(166, 153, 98, 28);
		panel.add(txtFieldCostOfDrinks);
		txtFieldCostOfDrinks.setColumns(10);
		
		JLabel lblTotal = new JLabel("Total:");
		lblTotal.setHorizontalAlignment(SwingConstants.CENTER);
		lblTotal.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 17));
		lblTotal.setBounds(15, 334, 125, 22);
		panel.add(lblTotal);
		
		txtFieldTotal = new JTextField();
		txtFieldTotal.setBounds(166, 328, 98, 28);
		panel.add(txtFieldTotal);
		txtFieldTotal.setColumns(10);
		
		JLabel lblBill = new JLabel("Account");
		lblBill.setForeground(Color.BLACK);
		lblBill.setHorizontalAlignment(SwingConstants.CENTER);
		lblBill.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 40));
		lblBill.setBounds(10, 47, 278, 38);
		panel.add(lblBill);

		JButton btnSubmit = new JButton("Submit ");
		btnSubmit.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 20));
		btnSubmit.setForeground(Color.BLACK);
		btnSubmit.setBounds(88, 452, 125, 38);
		panel.add(btnSubmit);
		
		JButton btnReset = new JButton("Reset");
		btnReset.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				quantitySalads.setText(null);
				quantitySoups.setText(null);
				quantityMainCourses.setText(null);
				quantityDesserts.setText(null);
				quantityHotDrinks.setText(null);
				quantityUncarbDrinks.setText(null);
				quantityCarbDrinks.setText(null);
				quantityAlcDrinks.setText(null);
				txtFieldCostOfMeal.setText(null);
				txtFieldCostOfDrinks.setText(null);
				txtFieldTotal.setText(null);
				saladsBox.setSelectedItem("Salads");
				soupsBox.setSelectedItem("Soups");
				mainCoursesBox.setSelectedItem("Main courses");
				dessertsBox.setSelectedItem("Desserts");
				hotDrinksBox.setSelectedItem("Hot drinks");
				uncarbonatedDrinksBox.setSelectedItem("Uncarbonated drinks");
				carbonatedDrinksBox.setSelectedItem("Carbonated drinks");
				alcoholDrinksBox.setSelectedItem("Alcohol drinks");
			}
		});
		btnReset.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 20));
		btnReset.setBounds(10, 11, 125, 38);
		frame.getContentPane().add(btnReset);
		JButton btnNewButton = new JButton("Receipt");
		btnNewButton.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 20));
		btnNewButton.setBounds(157, 12, 125, 38);
		frame.getContentPane().add(btnNewButton);
		
		JPanel panel_1 = new JPanel();
		panel_1.setBorder(new LineBorder(new Color(0, 0, 0), 5, true));
		panel_1.setBounds(1014, 103, 303, 534);
		frame.getContentPane().add(panel_1);
		panel_1.setLayout(null);
		
		JLabel lblReceipt = new JLabel("Receipt");
		lblReceipt.setFont(new Font("Sitka Heading", Font.BOLD | Font.ITALIC, 40));
		lblReceipt.setHorizontalAlignment(SwingConstants.CENTER);
		lblReceipt.setBounds(15, 48, 278, 38);
		panel_1.add(lblReceipt);
		
		txtReceipt = new JTextField();
		txtReceipt.setForeground(Color.BLACK);
		txtReceipt.setBounds(15, 97, 278, 426);
		panel_1.add(txtReceipt);
		txtReceipt.setColumns(10);
		
		JButton btnNewButton_1 = new JButton("New button");
		btnNewButton_1.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
			}
		});
		btnNewButton_1.setBounds(310, 11, 108, 38);
		frame.getContentPane().add(btnNewButton_1);
		btnSubmit.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				double costOfMeal = 0.0;
				double costOfDrinks = 0.0;
				// Salads:
				double numberOfSalads = Double.parseDouble(quantitySalads.getText());
				double costOfShopskaSalad = (3.50 * numberOfSalads);
				double costOfMixedSalad = (4.80 * numberOfSalads);
				double costOfShepSalad = (5.10 * numberOfSalads);
				if (saladsBox.getSelectedItem().equals("Shopska salad")) {
					costOfMeal += costOfShopskaSalad;
				}
				if (saladsBox.getSelectedItem().equals("Mixed salad")) {
					costOfMeal += costOfMixedSalad;
				}
				if (saladsBox.getSelectedItem().equals("Shepherd's salad salad")) {
					costOfMeal += costOfShepSalad;
				}

				// Soups:
				double numberOfSoups = Double.parseDouble(quantitySoups.getText());
				double costOfChickenSoup = (2.50 * numberOfSoups);
				double costOfMeatballSoup = (3.15 * numberOfSoups);
				double costOfVegetableSoup = (2.80 * numberOfSoups);
				if (soupsBox.getSelectedItem().equals("Chicken soup")) {
					costOfMeal += costOfChickenSoup;
				}
				if (soupsBox.getSelectedItem().equals("Meatball soup")) {
					costOfMeal += costOfMeatballSoup;
				}
				if (soupsBox.getSelectedItem().equals("Vegetable soup")) {
					costOfMeal += costOfVegetableSoup;
				}

				// Main courses:
				double numberOfMainMeals = Double.parseDouble(quantityMainCourses.getText());
				double costOfChickWithPotatoes = (5.20 * numberOfMainMeals);
				double costOfRice = (4.80 * numberOfMainMeals);
				double costOfSpaghetti = (6.30 * numberOfMainMeals);
				if (mainCoursesBox.getSelectedItem().equals("Chicken with potatoes")) {
					costOfMeal += costOfChickWithPotatoes;
				}
				if (mainCoursesBox.getSelectedItem().equals("Rice with vegetables")) {
					costOfMeal += costOfRice;
				}
				if (mainCoursesBox.getSelectedItem().equals("Spaghetti")) {
					costOfMeal += costOfSpaghetti;
				}

				// Desserts:
				double numberOfDesserts = Double.parseDouble(quantityDesserts.getText());
				double costOfIceCream = (1.50 * numberOfDesserts);
				double costOfPancake = (3.00 * numberOfDesserts);
				double costOfPumpkinPie = (4.00 * numberOfDesserts);
				if (dessertsBox.getSelectedItem().equals("Ice cream")) {
					costOfMeal += costOfIceCream;
				}
				if (dessertsBox.getSelectedItem().equals("Pancake")) {
					costOfMeal += costOfPancake;
				}
				if (dessertsBox.getSelectedItem().equals("Pumpkin pie")) {
					costOfMeal += costOfPumpkinPie;
				}

				// Hot drinks

				double numberOfHotDrinks = Double.parseDouble(quantityHotDrinks.getText());
				double costOfCoffee = (1.20 * numberOfHotDrinks);
				double costOfHotChoc = (1.80 * numberOfHotDrinks);
				double costOfCappuccino = (2.00 * numberOfHotDrinks);
				double costOfLatte = (2.10 * numberOfHotDrinks);
				double costOfMilk = (1.00 * numberOfHotDrinks);
				if (hotDrinksBox.getSelectedItem().equals("Coffee")) {
					costOfDrinks += costOfCoffee;
				}
				if (hotDrinksBox.getSelectedItem().equals("Hot chocolate")) {
					costOfDrinks += costOfHotChoc;
				}
				if (hotDrinksBox.getSelectedItem().equals("Cappuccino")) {
					costOfDrinks += costOfCappuccino;
				}
				if (hotDrinksBox.getSelectedItem().equals("Latte")) {
					costOfDrinks += costOfLatte;
				}
				if (hotDrinksBox.getSelectedItem().equals("Milk")) {
					costOfDrinks += costOfMilk;
				}

				// Uncarbonated drinks
				double numberOfUncarbDrinks = Double.parseDouble(quantityUncarbDrinks.getText());
				double costOfWater = (1.00 * numberOfUncarbDrinks);
				double costOfOrangeJuice = (1.80 * numberOfUncarbDrinks);
				double costOfAppleJuice = (1.70 * numberOfUncarbDrinks);
				double costOfBananaJuice = (1.60 * numberOfUncarbDrinks);
				double costOfPeachJuice = (1.40 * numberOfUncarbDrinks);
				double costOfAppricotJuice = (1.50 * numberOfUncarbDrinks);
				if (uncarbonatedDrinksBox.getSelectedItem().equals("Water")) {
					costOfDrinks += costOfWater;
				}
				if (uncarbonatedDrinksBox.getSelectedItem().equals("Orange juice")) {
					costOfDrinks += costOfOrangeJuice;
				}
				if (uncarbonatedDrinksBox.getSelectedItem().equals("Apple juice")) {
					costOfDrinks += costOfAppleJuice;
				}
				if (uncarbonatedDrinksBox.getSelectedItem().equals("Banana juice")) {
					costOfDrinks+= costOfBananaJuice;
				}
				if (uncarbonatedDrinksBox.getSelectedItem().equals("Peach juice")) {
					costOfDrinks += costOfPeachJuice;
				}
				if (uncarbonatedDrinksBox.getSelectedItem().equals("Appricot juice")) {
					costOfDrinks += costOfAppricotJuice;
				}

				// Carbonated drinks
				double numberOfCarbDrinks = Double.parseDouble(quantityUncarbDrinks.getText());
				double costOfCocaCola = (1.00 * numberOfCarbDrinks);
				double costOfFanta = (1.80 * numberOfCarbDrinks);
				double costOfSprite = (1.70 * numberOfCarbDrinks);
				double costOfTonic = (1.60 * numberOfCarbDrinks);
				if (carbonatedDrinksBox.getSelectedItem().equals("Coca Cola")) {
					costOfDrinks += costOfCocaCola;
				}
				if (carbonatedDrinksBox.getSelectedItem().equals("Fanta")) {
					costOfDrinks += costOfFanta;
				}
				if (carbonatedDrinksBox.getSelectedItem().equals("Sprite")) {
					costOfDrinks += costOfSprite;
				}
				if (carbonatedDrinksBox.getSelectedItem().equals("Tonic")) {
					costOfDrinks += costOfTonic;
				}

				// Alcohol
				double numberOfAlcDrinks = Double.parseDouble(quantityAlcDrinks.getText());
				double costOfWhiskey = (4.20 * numberOfAlcDrinks);
				double costOfVodka = (3.90 * numberOfAlcDrinks);
				double costOfRedWine = (5.40 * numberOfAlcDrinks);
				double costOfWhiteWine = (6.60 * numberOfAlcDrinks);
				double costOfGin = (4.10 * numberOfAlcDrinks);
				if (alcoholDrinksBox.getSelectedItem().equals("Whiskey")) {
					costOfDrinks += costOfWhiskey;
				}
				if (alcoholDrinksBox.getSelectedItem().equals("Vodka")) {
					costOfDrinks += costOfVodka;
				}
				if (alcoholDrinksBox.getSelectedItem().equals("Red wine")) {
					costOfDrinks += costOfRedWine;
				}
				if (alcoholDrinksBox.getSelectedItem().equals("White wine")) {
					costOfDrinks += costOfWhiteWine;
				}

				if (alcoholDrinksBox.getSelectedItem().equals("Gin")) {
					costOfDrinks += costOfGin;
				}


				String shownCostOfMeal = String.format("%.2f", costOfMeal);
				txtFieldCostOfMeal.setText(shownCostOfMeal);
				String shownCostOfDrinks = String.format("%.2f", costOfDrinks);
				txtFieldCostOfDrinks.setText(shownCostOfDrinks);
				double account = costOfMeal + costOfDrinks;
				String shownTotal = String.format("%.2f", account);
				txtFieldTotal.setText(shownTotal);
				
				
			}
		});
	}
}
