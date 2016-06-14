package samples.number;

public class KinshuSample {
  public static final int[] YEN_TYPES = {
    10000,5000,1000,500,100,50,10,5,1
  };
  public static int[] getYenCount(int yen, int[] yentype) {
    int[] count = new int[yentype.length];
    for (int i = 0; i < yentype.length; i++) {
      while (yen >= yentype[i]) {
        yen -= yentype[i];
        count[i]++;
      }
    }
    return count;
  }
  public static void main(String[] args) {
    int yen = 87654;
    int[] count = getYenCount(yen, YEN_TYPES);
    for (int i = 0; i < YEN_TYPES.length; i++) {
      System.out.println(YEN_TYPES[i] + "‰~\t" + count[i] + "–‡");
    }
  }
}