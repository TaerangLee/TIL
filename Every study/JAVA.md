# 9/6
## 자바프로그램이 (원기둥 넓이/ 원 넓이 구하기)

    package chap06;

    public class CircleExample {

        public static void main(String[] args) {
            
            
            Circle c1 = new Circle();
            System.out.println(c1.getRadius());
            c1.printNeolbEe();
            
            Wonggidung w1=new Wonggidung();
            System.out.println("반지름" + w1.getRadius()+", 높이"+ w1.getheight());
            w1.printNeolbEe();
            
            
        }

    }

    class Circle {
        
        protected int radius = 10;  //반지름
        
        private void superMethod() {
            System.out.println("해당 메소드는...??? 클래스 내부(설계도)에서만 사용이 가능합니다.");
        }
        
        protected int getRadius() {
            return this.radius;
        }
        
        public void printNeolbEe() {
            System.out.println("넓이" + radius * radius * 3.14);
        }
        
        
    }


    class Wonggidung extends Circle {             //Circle 이라는 class 라는 상속을 받음.
        
        int height = 10;
        int getheight() {
            return this.height;
        }
        
        public void printNeolbEe() {  //메소드 오버라이딩 (재정의)
            System.out.println("넓이"+2*(radius * radius * 3.14)+(2*3.14)+(2*3.14 * radius) * height);
        }
    }