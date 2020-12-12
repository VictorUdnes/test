public class getEvenDigitSum {

    public static int getEvenDigitSum (int number) {
        int i = 1;
        int sum = 0;
        int prevDigits = 0;

          while (prevDigits < number){
              i *=10;
              int x = number% i;
              x -= prevDigits;
              x = x / (i/10);

              if (x%2 == 0) {
                  sum += x;
              }
              x = x * (i/10);
              prevDigits += x;

          }

          if (number > 0) {
              return sum;
        } else return -1;

    }

    public static void main(String[] args) {
        System.out.println(getEvenDigitSum(123456789));
    }
}
