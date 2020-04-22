MadPay 724 AspNetCore SDK

[![Build status](https://img.shields.io/appveyor/ci/keyone2693/imageresizer-aspnetcore)](https://img.shields.io/appveyor/build/keyone2693/madpay724-aspnetcore-gateway)
[![NuGet](https://img.shields.io/nuget/v/MadPay724.AspNetCore.GateWay)](https://www.nuget.org/packages/MadPay724.AspNetCore.GateWay/)
[![GitHub issues](https://img.shields.io/github/issues/MadPay-724/MadPay724.AspNetCore.GateWay)](https://github.com/MadPay-724/MadPay724.AspNetCore.GateWay/issues)
[![GitHub stars](https://img.shields.io/github/stars/MadPay-724/MadPay724.AspNetCore.GateWay)](https://github.com/MadPay-724/MadPay724.AspNetCore.GateWay/stargazers)
[![GitHub license](https://img.shields.io/github/license/MadPay-724/MadPay724.AspNetCore.GateWay)](https://github.com/MadPay-724/MadPay724.AspNetCore.GateWay/blob/master/LICENSE)

#### Current version: 1.1.x [Stable]


# Wiki

for using this awesome library, you only need to add two things

first:
add this line of code to your Startup.cs


```c#
public void ConfigureServices(IServiceCollection services)
{
  //...
  services.AddMadpay724GateWay();
  //...
}
```

Then inject in your class constrauctor :

```c#
public class Test
{
  private readonly IMadPayGateWay _gateWay;
  public Test(IMadPayGateWay gateWay)
  {
    _gateWay=gateWay;
  }
```

at the end use three method that provided (pay | verify | refund) :


