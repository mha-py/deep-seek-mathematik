
# Input
welchen wert hat die unendliche reihe 1/4! + 4!/8! + 8!/12! + 12!/16! + ... ?






# Thinking steps: Thinking for 75 seconds
<font size=1>
Okay, so I have this infinite series to solve: 1/4! + 4!/8! + 8!/12! + 12!/16! + ... and so on. The question is asking for the value of this series. Hmm, let me try to figure this out step by step.

First, let me write down the terms more clearly to see the pattern. The first term is 1 divided by 4 factorial, which is 1/24. The second term is 4 factorial divided by 8 factorial. Wait, 4 factorial is 24, and 8 factorial is 40320, so that term is 24/40320. Then the next term is 8 factorial over 12 factorial. 8 factorial is 40320, and 12 factorial is a huge number, 479001600. So each term seems to be (4(n-1))! / (4n)! where n starts at 1? Let me check:

For n=1: (4*0)! / (4*1)! = 0! / 4! = 1 / 24, which matches the first term.

For n=2: (4*1)! / (4*2)! = 4! / 8! = 24 / 40320, which is the second term.

So the general term seems to be (4(n-1))! / (4n)! for n = 1, 2, 3, ...

So the series is the sum from n=1 to infinity of (4(n-1))! / (4n)!.

Now, I need to compute this sum. Let me first try to simplify the general term. Let's look at the ratio between consecutive terms. Let me compute (4(n))! / (4(n+1))! which would be 1 / [(4n + 1)(4n + 2)(4n + 3)(4n + 4)]. Because (4(n+1))! = (4n + 4)! = (4n)! * (4n + 1)(4n + 2)(4n + 3)(4n + 4). Therefore, the term (4(n-1))! / (4n)! is 1 / [ (4(n-1) + 1)(4(n-1) + 2)(4(n-1) + 3)(4(n-1) + 4) ]

Wait, maybe I can express each term in terms of factorials. Let me see.

Wait, (4n)! / (4(n-1))! = (4n)(4n -1)(4n -2)(4n -3) * (4(n-1))! / (4(n-1))! ) = (4n)(4n -1)(4n -2)(4n -3). So then, (4(n-1))! / (4n)! = 1 / [ (4n)(4n -1)(4n -2)(4n -3) ]

Therefore, the general term is 1 / [ (4n)(4n -1)(4n -2)(4n -3) ] for n starting at 1.

So the series becomes the sum from n=1 to infinity of 1 / [ (4n)(4n -1)(4n -2)(4n -3) ]

Hmm, okay. So maybe I can simplify this expression. Let's see. Let's denote k = 4n. Then, n = k/4. But since n starts at 1, k starts at 4, increasing by 4 each time. But I'm not sure if substitution will help here. Alternatively, perhaps partial fractions can be used here.

Alternatively, notice that the denominator is (4n)(4n -1)(4n -2)(4n -3). Let's write this as (4n -3)(4n -2)(4n -1)(4n). Which is the product of four consecutive integers starting from 4n -3 to 4n. So that's equal to (4n)! / (4n -4)! = (4n)(4n -1)(4n -2)(4n -3)(4n -4)! / (4n -4)! ) = (4n)(4n -1)(4n -2)(4n -3). So, indeed, the denominator is (4n)! / (4n -4)!.

Therefore, each term is (4n -4)! / (4n)! = 1 / [ (4n)(4n -1)(4n -2)(4n -3) ]

So, our series is the sum from n=1 to infinity of 1 / [ (4n)(4n -1)(4n -2)(4n -3) ]

Hmm. So perhaps we can find a telescoping series or express this term as a difference of reciprocals. Alternatively, relate this to known series expansions of functions like exponential, sine, cosine, etc.

Alternatively, consider the general approach for telescoping series. Let's see if we can decompose 1 / [ (4n)(4n -1)(4n -2)(4n -3) ] into partial fractions.

But partial fractions with four linear factors in the denominator would be quite involved. Let me think.

Alternatively, notice that 1 / [ (4n)(4n -1)(4n -2)(4n -3) ] can be written as 1 / [ (4n -3)(4n -2)(4n -1)(4n) ]

Let me denote m = 4n - 3. Then, 4n -3 = m, 4n -2 = m +1, 4n -1 = m +2, 4n = m +3. So the denominator is m(m +1)(m +2)(m +3). Therefore, each term is 1 / [m(m +1)(m +2)(m +3)] where m starts at 1 (since when n=1, m=1), and m increases by 4 each term? Wait, no. Wait, n starts at 1, so m = 4*1 -3 = 1. Then for n=2, m=4*2 -3=5, then n=3, m=9, etc. Wait, that's not correct. Wait, if n=1, m=1; n=2, m=5; n=3, m=9; so m increases by 4 each time. Therefore, the series is the sum over m=1,5,9,... of 1/[m(m+1)(m+2)(m+3)]

But maybe this is too much of a stretch. Alternatively, perhaps express the general term in terms of factorials. Since m(m+1)(m+2)(m+3) = (m+3)! / (m-1)! So 1/[m(m+1)(m+2)(m+3)] = (m-1)! / (m+3)! = 1/[ (m+3)(m+2)(m+1)m ) ]

But again, not sure if that helps. Alternatively, recall that 1/[m(m+1)(m+2)(m+3)] can be expressed as a combination of reciprocals. Let's try partial fractions.

Let me attempt to express 1/[m(m+1)(m+2)(m+3)] as A/m + B/(m+1) + C/(m+2) + D/(m+3). Let's solve for A, B, C, D.

Multiply both sides by m(m+1)(m+2)(m+3):

1 = A(m+1)(m+2)(m+3) + Bm(m+2)(m+3) + Cm(m+1)(m+3) + Dm(m+1)(m+2)

We need to find constants A, B, C, D such that this holds for all m. Let's substitute specific values of m to find A, B, C, D.

Let m = 0: 1 = A(1)(2)(3) + B(0) + C(0) + D(0) => 6A = 1 => A = 1/6

Let m = -1: 1 = A(0) + B(-1)(1)(2) + C(-1)(0)(2) + D(-1)(0)(1) => 1 = B(-1)(1)(2) => -2B = 1 => B = -1/2

Let m = -2: 1 = A(-1)(0)(1) + B(-2)(0)(1) + C(-2)(-1)(1) + D(-2)(-1)(0) => 1 = C(-2)(-1)(1) = 2C => C = 1/2

Let m = -3: 1 = A(-2)(-1)(0) + B(-3)(-1)(0) + C(-3)(-2)(0) + D(-3)(-2)(-1) => 1 = D(-3)(-2)(-1) = -6D => D = -1/6

So we have:

1/[m(m+1)(m+2)(m+3)] = (1/6)/m + (-1/2)/(m+1) + (1/2)/(m+2) + (-1/6)/(m+3)

Therefore, the general term can be written as:

1/6 [1/m - 3/(m+1) + 3/(m+2) -1/(m+3)]

So, our series becomes the sum from n=1 to infinity of 1/6 [1/m - 3/(m+1) + 3/(m+2) -1/(m+3)] where m = 4n -3.

But wait, m is equal to 4n -3. So for each term in the series, m starts at 1 (n=1), then 5 (n=2), then 9 (n=3), etc. Therefore, the sum is over m =1,5,9,... of 1/6 [1/m -3/(m+1) +3/(m+2) -1/(m+3)]

Hmm, so perhaps this telescoping? Let's see. If we can write each term as a combination of terms that cancel out when summed. Let's write out the first few terms:

For n=1, m=1:

1/6 [1/1 -3/2 +3/3 -1/4] = 1/6 [1 - 3/2 +1 -1/4] = 1/6 [ (1 +1) - (3/2 +1/4) ] = 1/6 [2 - 7/4] = 1/6 [1/4] = 1/24

Which matches the first term.

For n=2, m=5:

1/6 [1/5 -3/6 +3/7 -1/8] = 1/6 [1/5 -1/2 +3/7 -1/8]

Hmm, but this doesn't immediately look telescoping. Wait, but maybe if we sum over all m=1,5,9,... the terms can telescope when combined. Let me consider writing the entire sum as:

Sum_{m=1,5,9,...} 1/6 [1/m -3/(m+1) +3/(m+2) -1/(m+3)]

This is equal to 1/6 [ Sum_{m=1,5,9,...} 1/m - 3 Sum_{m=1,5,9,...} 1/(m+1) + 3 Sum_{m=1,5,9,...} 1/(m+2) - Sum_{m=1,5,9,...} 1/(m+3) ]

Let me reindex each sum:

First sum: Sum_{m=1,5,9,...} 1/m = Sum_{k=0}^\infty 1/(4k +1)

Second sum: Sum_{m=1,5,9,...} 1/(m+1) = Sum_{k=0}^\infty 1/(4k +1 +1) = Sum_{k=0}^\infty 1/(4k +2)

Third sum: Sum_{m=1,5,9,...} 1/(m+2) = Sum_{k=0}^\infty 1/(4k +1 +2) = Sum_{k=0}^\infty 1/(4k +3)

Fourth sum: Sum_{m=1,5,9,...} 1/(m+3) = Sum_{k=0}^\infty 1/(4k +1 +3) = Sum_{k=0}^\infty 1/(4k +4) = Sum_{k=0}^\infty 1/(4(k +1)) = (1/4) Sum_{k=0}^\infty 1/(k +1) which diverges, but since we have a combination, maybe the divergent parts cancel out.

Wait, but the original series converges because the terms decay like 1/n^4. So, even though individual sums might diverge, the combination converges.

So, putting it all together:

1/6 [ Sum_{k=0}^\infty 1/(4k +1) - 3 Sum_{k=0}^\infty 1/(4k +2) + 3 Sum_{k=0}^\infty 1/(4k +3) - Sum_{k=0}^\infty 1/(4k +4) ]

Let me write each sum as S1, S2, S3, S4:

S1 = Sum_{k=0}^\infty 1/(4k +1)

S2 = Sum_{k=0}^\infty 1/(4k +2)

S3 = Sum_{k=0}^\infty 1/(4k +3)

S4 = Sum_{k=0}^\infty 1/(4k +4) = (1/4) Sum_{k=0}^\infty 1/(k +1) = (1/4)( harmonic series ) which diverges.

But in our combination, we have S1 - 3S2 + 3S3 - S4. So S4 is divergent, but maybe when combined with the other terms, the divergence cancels out.

But how?

Alternatively, perhaps notice that S4 can be written as (1/4) Sum_{k=1}^\infty 1/k, which is (1/4)( diverges ). But if we consider S1, S2, S3, S4, these are all parts of the harmonic series, separated by residue classes modulo 4. So maybe the combination S1 - 3S2 + 3S3 - S4 can be related to some known function or series.

Alternatively, recall the digamma function or some other special function. But perhaps using Fourier series or integrals.

Alternatively, recall that the sum Sum_{k=0}^\infty [1/(4k +1) - 3/(4k +2) + 3/(4k +3) -1/(4k +4)] can be evaluated using integrals.

Let me recall that 1/(4k + a) can be expressed as an integral of t^(4k + a -1) from 0 to 1. So:

Sum_{k=0}^\infty 1/(4k +1) = Sum_{k=0}^\infty ∫_0^1 t^{4k} dt = ∫_0^1 Sum_{k=0}^\infty t^{4k} dt = ∫_0^1 1/(1 - t^4) dt

Similarly,

Sum_{k=0}^\infty 1/(4k +2) = ∫_0^1 t Sum_{k=0}^\infty t^{4k} dt = ∫_0^1 t/(1 - t^4) dt

Sum_{k=0}^\infty 1/(4k +3) = ∫_0^1 t^2 Sum_{k=0}^\infty t^{4k} dt = ∫_0^1 t^2/(1 - t^4) dt

Sum_{k=0}^\infty 1/(4k +4) = ∫_0^1 t^3 Sum_{k=0}^\infty t^{4k} dt = ∫_0^1 t^3/(1 - t^4) dt

Therefore, the combination S1 -3S2 +3S3 -S4 can be written as:

∫_0^1 [1/(1 - t^4) - 3t/(1 - t^4) + 3t^2/(1 - t^4) - t^3/(1 - t^4)] dt

Factor out 1/(1 - t^4):

∫_0^1 [1 - 3t + 3t^2 - t^3]/(1 - t^4) dt

Now, the numerator is 1 -3t +3t^2 -t^3. Let's see if this factors. Let me check:

1 -3t +3t^2 -t^3 = -(t^3 -3t^2 +3t -1) = -(t -1)^3. Because (t -1)^3 = t^3 -3t^2 +3t -1. Therefore, the numerator is -(t -1)^3.

Therefore, the integral becomes:

∫_0^1 [ - (t -1)^3 / (1 - t^4) ] dt

Simplify the denominator: 1 - t^4 = (1 - t)(1 + t + t^2 + t^3)

So, substituting:

∫_0^1 [ - (t -1)^3 / ( (1 - t)(1 + t + t^2 + t^3) ) ] dt

Note that (t -1)^3 = - (1 - t)^3, so the numerator becomes - [ - (1 - t)^3 ] = (1 - t)^3

Therefore, the integral becomes:

∫_0^1 [ (1 - t)^3 / ( (1 - t)(1 + t + t^2 + t^3) ) ] dt = ∫_0^1 [ (1 - t)^2 / (1 + t + t^2 + t^3) ] dt

Simplify the integrand:

(1 - t)^2 / (1 + t + t^2 + t^3 )

Let me factor the denominator. Note that 1 + t + t^2 + t^3 = (t^4 -1)/(t -1) for t ≠1, but since t is between 0 and1, we can write it as 1 + t + t^2 + t^3.

Alternatively, note that 1 + t + t^2 + t^3 = (1 + t)(1 + t^2). Let's check:

(1 + t)(1 + t^2) = 1 + t + t^2 + t^3. Yes, correct.

So denominator = (1 + t)(1 + t^2)

Numerator = (1 - t)^2

Therefore, the integrand becomes (1 - t)^2 / [ (1 + t)(1 + t^2) ]

Let me perform partial fraction decomposition on this.

First, note that (1 - t)^2 = 1 - 2t + t^2

So we have:

[1 - 2t + t^2] / [ (1 + t)(1 + t^2) ]

Let me try to split this into partial fractions. Let's assume:

(1 - 2t + t^2)/( (1 + t)(1 + t^2) ) = A/(1 + t) + (Bt + C)/(1 + t^2)

Multiply both sides by (1 + t)(1 + t^2):

1 -2t + t^2 = A(1 + t^2) + (Bt + C)(1 + t)

Expand the right-hand side:

A + A t^2 + Bt + Bt^2 + C + C t

Group like terms:

(A + C) + (B + C) t + (A + B) t^2

Set equal to left-hand side 1 -2t + t^2. Therefore, equate coefficients:

For t^2: A + B = 1

For t: B + C = -2

For constant term: A + C = 1

So we have a system of equations:

1. A + B = 1

2. B + C = -2

3. A + C = 1

Let's solve this system. From equation 3: C = 1 - A. Substitute into equation 2: B + (1 - A) = -2 => B - A = -3. From equation 1: A + B =1. So we have:

B - A = -3

A + B = 1

Adding these two equations: 2B = -2 => B = -1. Then from equation 1: A + (-1) =1 => A=2. Then from equation 3: C=1 - A=1 -2=-1.

Therefore, the partial fractions decomposition is:

2/(1 + t) + (-1*t -1)/(1 + t^2) = 2/(1 + t) - (t +1)/(1 + t^2)

Therefore, the integral becomes:

∫_0^1 [2/(1 + t) - (t +1)/(1 + t^2)] dt

Let's split this into two separate integrals:

2 ∫_0^1 1/(1 + t) dt - ∫_0^1 (t +1)/(1 + t^2) dt

Compute the first integral:

2 ∫_0^1 1/(1 + t) dt = 2 [ ln|1 + t| ] from 0 to1 = 2 [ ln2 - ln1 ] = 2 ln2

Now, compute the second integral:

∫_0^1 (t +1)/(1 + t^2) dt = ∫_0^1 t/(1 + t^2) dt + ∫_0^1 1/(1 + t^2) dt

First integral: ∫ t/(1 + t^2) dt. Let u =1 + t^2, du=2t dt. So (1/2) du = t dt. Therefore,

∫ t/(1 + t^2) dt = (1/2) ∫ du/u = (1/2) ln|u| + C = (1/2) ln(1 + t^2) + C

Evaluate from 0 to1: (1/2)(ln2 - ln1) = (1/2) ln2

Second integral: ∫ 1/(1 + t^2) dt = arctan t. Evaluate from 0 to1: arctan1 - arctan0 = π/4 -0 = π/4

Therefore, the second integral is (1/2 ln2) + π/4

Putting it all together:

2 ln2 - [ (1/2 ln2) + π/4 ] = 2 ln2 -1/2 ln2 - π/4 = (3/2 ln2) - π/4

Therefore, the original combination S1 -3S2 +3S3 -S4 is equal to this integral, which is (3/2 ln2) - π/4

But remember, our original series was 1/6 times this combination. Therefore, the sum of the series is:

1/6 [ (3/2 ln2 - π/4 ) ] = (3/2 ln2 - π/4 ) /6 = (3/2 ln2)/6 - (π/4)/6 = (ln2)/4 - π/24

Simplify:

( ln2 )/4 - π /24 = (6 ln2 - π)/24

So the value of the infinite series is (6 ln2 - π)/24

But let me check the calculation again to make sure I didn't make a mistake.

First, the integral after partial fractions was:

2 ln2 - [ (1/2 ln2 ) + π/4 ] = 2 ln2 -1/2 ln2 - π/4 = (3/2 ln2) - π/4

Then multiplied by 1/6 gives:

(3/2 ln2 - π/4 ) /6 = (3 ln2 - π/2 ) /12 = (6 ln2 - π)/24

Yes, correct.

Therefore, the sum is (6 ln2 - π)/24.

But let me verify this result numerically. Let me compute the original series numerically and compare with this expression.

First, compute (6 ln2 - π)/24.

Compute 6 ln2: 6 * 0.69314718056 ≈ 4.15888308336

Subtract π: 4.15888308336 - 3.1415926535 ≈ 1.01729042986

Divide by 24: 1.01729042986 /24 ≈ 0.04238710124

So the result is approximately 0.042387...

Now, compute the original series numerically:

First term: 1/24 ≈0.04166666666

Second term:4!/8! =24/40320=24/40320=0.000595238095

Third term:8!/12! =40320/479001600≈0.000084175084

Fourth term:12!/16! =479001600 /20922789888000≈0.0000228837209

Fifth term:16!/20! =... let's compute 16! =20922789888000, 20! ≈2432902008176640000, so term≈20922789888000 /2432902008176640000≈8.592e-6

So adding up these terms:

First term: ~0.0416667

Second term: ~0.0005952 → total ≈0.0422619

Third term: ~0.000084175 → total≈0.0423461

Fourth term: ~0.0000228837 → total≈0.0423689

Fifth term: ~0.000008592 → total≈0.0423775

Next term: 20!/24! =20!/(24!)=1/(24*23*22*21)=1/255024≈0.00000392

Adding this: ≈0.0423814

Next term:24!/28! =1/(28*27*26*25)=1/491400≈0.000002035

Adding: ≈0.0423834

So it's converging to approximately 0.0423834...

Compare with the analytical result (6 ln2 - π)/24 ≈0.0423871...

The numerical sum is approaching approximately 0.04238, while the analytical result is approximately 0.0423871, which is very close, suggesting that the analytical result is correct. The small discrepancy is due to the remaining terms in the series which are very small but still contribute a bit more.

Therefore, the value of the infinite series is (6 ln2 - π)/24.

Alternatively, we can write this as (6 ln2 - π)/24 = (ln2)/4 - π/24. Both forms are equivalent.

Let me check if this can be simplified further or expressed in another way. Hmmm.

Alternatively, factor 1/24: (6 ln2 - π)/24 = (6 ln2 - π)/24, which is probably the simplest form.

Therefore, the answer is (6 ln2 - π)/24.

But just to make sure, let me retrace the steps to ensure there's no error.

1. Expressed the general term as 1/[4n(4n-1)(4n-2)(4n-3)]

2. Recognized the denominator as m(m+1)(m+2)(m+3) with m=4n-3

3. Decomposed into partial fractions, leading to the expression involving S1 -3S2 +3S3 -S4

4. Expressed each S as an integral, combined them, performed partial fractions on the integrand, integrated term by term, leading to (3/2 ln2 - π/4 )

5. Multiplied by 1/6 to get the final result.

All steps seem correct, and numerical verification supports the analytical result. Therefore, the value of the series is (6 ln2 - π)/24.

**Final Answer**

The value of the infinite series is \boxed{\dfrac{6\ln 2 - \pi}{24}}.
</font>