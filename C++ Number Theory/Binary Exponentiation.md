// Calculating a^b
int bin_exp(int a, int b,int mod){
    int ans = 1;
    while (b)
    {
        if(b&1){
            ans = (1LL*ans*a)%mod;
        }
        a = (1LL*a*a)%mod;
        b = b>>1;
    }
    return ans;
}