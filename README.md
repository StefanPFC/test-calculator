import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

public class CalculatorTest {
    
    // Testiranje ispravnog rezultata 10 + 8 * 8 = 74 + prioritet mnozenja spram sabiranja
    public void testCalculate() {

        List<Float> numbers = new ArrayList<>(Arrays.asList(2.0f, 3.0f, 4.0f));
        List<String> operations = new ArrayList<>(Arrays.asList("+", "*", "-"));

        Calculator.Calculate(numbers, operations);

        float actualResult = Calculator.finalResult;
        float expectedResult = 74; 

        if (expectedResult == actualResult){
            System.out.println("Expected result: "+expectedResult+" Acctual result: "+actualResult+" Test: PASS!");
        }else{
            System.out.println("Expected result: "+expectedResult+" Acctual result: "+actualResult+" Test: FAIL!");
        };
    }
    
    public static void main(String[] args) {
        CalculatorTest calculatorTest = new CalculatorTest();
        calculatorTest.testCalculate();
    }
}
