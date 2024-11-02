# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Binomial nonlinear regression models Use bnlr (gnlm) With (In) R Software
install.packages("gnlm")
library("gnlm")
bnlr = read.csv("https://raw.githubusercontent.com/timbulwidodostp/bnlr/main/bnlr/bnlr.csv",sep = ";")
# Estimation Binomial nonlinear regression models Use bnlr (gnlm) With (In) R Software
Dependen <- cbind(bnlr$Dependen,10-bnlr$Dependen)
dose <- log10(100/c(bnlr$Independen))
bnlr_1 <- bnlr(Dependen, mu=~dose, pmu=c(1,1))
bnlr_1
bnlr_2 <- bnlr(Dependen, link="log log", mu=~dose, pmu=c(1,1))
bnlr_2
bnlr_3 <- bnlr(Dependen, link="comp log log", mu=~dose, pmu=c(1,1))
bnlr_3
bnlr_4 <- bnlr(Dependen, link="Cauchy", mu=~dose, pmu=c(60,-30))
bnlr_4
bnlr_5 <- bnlr(Dependen, link="Student", mu=~dose, pmu=c(60,-30), pshape=0.1)
bnlr_5
# Binomial nonlinear regression models Use bnlr (gnlm) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished