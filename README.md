
    public double myPow(double x, int n) {
        if(x == 1 || x == -1 && n%2 == 0)
            return 1;
        
        if(n == -2147483648) return 0;
        
        if(x == -1 && n%2 != 0)
            return -1;
        
        if(n < 0){
            n = -n;
            x = 1 / x;
        }
        
        double s = 1.0;
        while(n > 0)
        {
            if( n % 2 != 0)
            {
                s = s*x;
            }
            x = x*x;
            n = n / 2; 
        }
        return s;
    }
