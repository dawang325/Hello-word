# Hello-word
My repository

public class Main {
    public static void main(String[] args) {
/*        Thread2 thread2 = new Thread2();
        Thread thread = new Thread(thread2);*/
        Thread1 thread1 = new Thread1();
        Thread1 thread2 = new Thread1();
        Thread1 thread3 = new Thread1();
        thread1.start();
        thread2.start();
        thread3.start();
    }
}
class Thread1 extends Thread{
    private  int a = 50;
    public void run() {
        for(int j=0;j<=50;j++){
            System.out.println(Thread.currentThread().getName()+"第"+j+"次执行，此时a="+a);
            a--;
        }
    }
}
class Thread2 implements Runnable{
    @Override
    public void run() {
        for (int i = 0; i <=50 ; i++) {
            System.out.println(Thread.currentThread().getName()+i+"在执行");
        }
    }
}
