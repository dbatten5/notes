# Initial thoughts

What do TFL want to know?
- How much demand to expect during peak commuting hours in the evening
- What external factors will affect the distribution

What to include?
1. Distribution of bike hires during peak commuting times in the evening in the
spring and summer - is it normal? Should test each season separately. Should use
at least two "goodness-of-fit" tests
2. How distribution differs during spring and summer (or are they the same)

### 1.

What is $H_0$ for part 1.? The distribution follows a normal distribution for
spring and summer? $H_1$ that it isn't an normal distribution - then what?

Chi square test looks a possible test to use. Can only be used for data put into
classes (bins), good here as there are classified by hour or day.

Kolmogorov-Smirnov also looks like a good option - tells us when a sample is
unlikely to have a normal distribution. However, recommended for large samples
over 2000 (we only have 2 years worth of data $\approx$ 700 samples). For
smaller samples sizes, recommended to use the Shapiro-Wilk test (also known as
Ryan-Joiner).

Questions?
- Any separation of casual and registered users?
- How do we want to include the external factors? (Weather, windspeed, humidity)

### 2.
