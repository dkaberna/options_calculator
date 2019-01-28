# Makefile for Writing Make Files Example

# *****************************************************
# Variables to control Makefile operation

CXX = g++
DEBUG_LEVEL     = -g
EXTRA_CCFLAGS   = -Wall
CXXFLAGS        = -std=c++1z $(DEBUG_LEVEL) $(EXTRA_CCFLAGS) -I$(BOOST_ROOT)


#CXXFLAGS = -std=c++11 -I$(BOOST_ROOT)
LDFLAGS = -L$(BOOST_ROOT)/boost_output/lib -lboost_filesystem

# Boost C++ library
BOOST_ROOT = /usr/local/include/boost/boost_1_64_0#/boost_output/include/boost
#LIBS=-L/usr/local/include/boost/boost_1_64_0/boost_output/lib -lboost_filesystem
# ****************************************************
# Targets needed to bring the executable up to date

TestMain: TestMain.o PricingEngine.o StatisticalDistribution.o NormalDistribution.o \
	Mesher.o ExactSolutionBSEngine.o VanillaOption.o EuropeanOption.o \
	AmericanOption.o PerpetualAmericanOption.o
	
	$(CXX) $(CXXFLAGS) $(LDFLAGS) -o TestMain TestMain.o PricingEngine.o StatisticalDistribution.o NormalDistribution.o \
		Mesher.o ExactSolutionBSEngine.o VanillaOption.o EuropeanOption.o \
		AmericanOption.o PerpetualAmericanOption.o

clean:
	rm TestMain.o PricingEngine.o StatisticalDistribution.o NormalDistribution.o \
	Mesher.o ExactSolutionBSEngine.o VanillaOption.o EuropeanOption.o \
	AmericanOption.o PerpetualAmericanOption.o