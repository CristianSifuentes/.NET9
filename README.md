# What's New in .NET 9

## Overview
.NET 9, the successor to .NET 8, focuses on **cloud-native apps** and **performance**. It is a **standard-term support (STS)** release, supported for **18 months**.

📥 **[Download .NET 9](https://dotnet.microsoft.com/download/dotnet/9.0)**  
🗣 **[Discuss .NET 9 on GitHub Discussions](https://github.com/dotnet/runtime/discussions)**  

---

## Table of Contents

- [Runtime](#runtime)
- [Libraries](#libraries)
- [SDK](#sdk)
- [AI Building Blocks](#ai-building-blocks)
- [ASP.NET Core](#aspnet-core)
- [Entity Framework Core](#ef-core)
- [C# 13](#csharp-13)
- [F# 9](#fsharp-9)
- [Windows Forms & WPF](#windows-forms--wpf)
- [Diagnostics](#diagnostics)
- [Networking](#networking)
- [System.Text.Json](#systemtextjson)
- [Containers](#containers)
- [Code Analysis](#code-analysis)

---

## Runtime

### 🔹 Feature Switches with Trimming Support
New attributes for **feature switches** help toggle areas of functionality and **reduce app size** when trimming.

```csharp
[FeatureSwitchDefinition("Feature.IsSupported")]
internal static bool IsSupported => AppContext.TryGetSwitch("Feature.IsSupported", out bool isEnabled) ? isEnabled : true;
```

### 🔹 Garbage Collection Improvements
- **Dynamic adaptation to application sizes (DATAS)** enabled by default.
- **Performance boosts** with **loop optimizations**, **inline improvements**, and **Arm64 vectorization**.

📌 **[More details on .NET 9 runtime](https://learn.microsoft.com/dotnet/core/whats-new/dotnet-9#runtime)**

---

## Libraries

### 🔹 New LINQ Methods
- **CountBy()** and **AggregateBy()** optimize key-based aggregations without `GroupBy`.

```csharp
var counts = items.CountBy(item => item.Category);
```

- **New Collection Types**
  - `ReadOnlySet<T>` for immutable sets.
  - `OrderedDictionary<TKey, TValue>` maintains insertion order.

### 🔹 System.Text.Json Enhancements
- Support for **nullable reference types**.
- **Export JSON schemas** from types.
- Customize **indentation styles**.

📌 **[More details on .NET 9 libraries](https://learn.microsoft.com/dotnet/core/whats-new/dotnet-9#libraries)**

---

## SDK

### 🔹 New Features
- **Parallel unit testing** across target frameworks.
- `dotnet tool install` now supports **roll-forward** for compatibility.
- **Terminal logger improvements** for better test output and summaries.

📌 **[More details on .NET 9 SDK](https://learn.microsoft.com/dotnet/core/whats-new/dotnet-9#sdk)**

---

## AI Building Blocks

### 🔹 Tensor Enhancements
- New **`Tensor<T>`** type for **AI and ML applications**.
- **Optimized math operations** with `TensorPrimitives`.

```csharp
var tensor = Tensor.Create([1, 2, 3], [1, 3]);
```

### 🔹 AI Integration
- `Microsoft.Extensions.AI` for **large language models (LLMs)**.
- **ML.NET 4.0** includes **ONNX model streaming** and **TorchSharp support**.

📌 **[More details on AI features](https://learn.microsoft.com/dotnet/core/whats-new/dotnet-9#ai-building-blocks)**

---

## ASP.NET Core

### 🔹 Performance & Security Enhancements
- **Static file optimizations** with automatic fingerprinted versioning.
- **Blazor Updates**: Hybrid templates & new reconnection UX.
- **Native AOT Support** for APIs.

📌 **[More details on ASP.NET Core 9](https://learn.microsoft.com/dotnet/core/whats-new/dotnet-9#aspnet-core)**

---

## EF Core

- **Azure Cosmos DB Provider** improvements.
- **Pre-compiled queries** for better performance.

📌 **[More details on EF Core 9](https://learn.microsoft.com/dotnet/core/whats-new/dotnet-9#ef-core)**

---

## C# 13

### 🔹 New Features
- **`params` collections**.
- **New lock type and escape sequence `\e`**.
- **Implicit indexer access** in object initializers.

```csharp
var obj = new MyClass { [key] = value };
```

📌 **[More details on C# 13](https://learn.microsoft.com/dotnet/core/whats-new/dotnet-9#csharp-13)**

---

## F# 9

- **Nullable reference types**.
- **`Random` functions for collections**.
- **C# collection expressions** supported.

📌 **[More details on F# 9](https://learn.microsoft.com/dotnet/core/whats-new/dotnet-9#fsharp-9)**

---

## Windows Forms & WPF

- **Windows Fluent Theme** support.
- **Dark mode & accent colors** in WPF.
- **ShowDialogAsync()** for `Form` and `TaskDialog`.

📌 **[More details on WPF & WinForms](https://learn.microsoft.com/dotnet/core/whats-new/dotnet-9#windows-forms-and-wpf)**

---

## Containers

- **Support for insecure registries**.
- **Updated environment variables**.

📌 **[More details on Containers](https://learn.microsoft.com/dotnet/core/whats-new/dotnet-9#containers)**

---

## Code Analysis

- **New Analyzers** for:
  - Redundant `Length` arguments.
  - Ensuring correct `Stream.Read` usage.
  - Avoiding `Nullable<T>` in `ArgumentNullException.ThrowIfNull`.

📌 **[More details on .NET 9 Analyzers](https://learn.microsoft.com/dotnet/core/whats-new/dotnet-9#code-analysis)**

---

## 🔗 Additional Resources

- 📜 **[.NET 9 Vision](https://devblogs.microsoft.com/dotnet/our-vision-for-dotnet-9/)**
- 🔍 **[Full .NET 9 Release Notes](https://learn.microsoft.com/dotnet/core/whats-new/dotnet-9)**

---

🎉 **Enjoy .NET 9!** 🚀  
Contribute and discuss on [GitHub](https://github.com/dotnet/runtime/discussions).  
