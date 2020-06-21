public static long fibonacci3(int n) {
        if (n < 1) {
            return -1;
        }
        if (n == 1 || n == 2) {
            return 1;
        }

        long[] arr = new long[n];
        arr[0] = arr[1] = 1;		//第一个和第二个数据特殊处理
        for (int i = 2; i < n; i++) {		
            arr[i] = arr[i -2] + arr[i - 1];
            arr[n -1] = arr[i];		//数列第n个数  对应数组arr[n - 1]  因为数组下标是从0开始的
        }

       /* for (int a : arr) {
            System.out.println(a);    //可以得到整个的数列数据

        }*/

        return arr[n - 1];
    }