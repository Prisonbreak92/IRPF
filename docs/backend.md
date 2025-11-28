# RPF Backend System

IRPF uses a pluggable backend abstraction to support multiple RPF formats and tools.

---

## IRpfBackend Interface
```csharp
public interface IRpfBackend
{
    Task ExtractAsync(string inputRpf, string outputDir);
    Task ImportAsync(string rpf, string localPath, string destination);
    Task ReplaceFileAsync(string rpf, string localPath, string targetPath);
    Task<byte[]> ReadFileAsync(string rpf, string internalPath);
}
