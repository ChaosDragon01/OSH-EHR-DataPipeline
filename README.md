# OSH-EHR-DataPipeline
├── src/
│   ├── OSHEngine.Core/                 # Domain Models & Interfaces
│   │   ├── Models/
│   │   │   ├── StudentPayload.cs
│   │   │   └── IntegrationRecord.cs
│   │   └── Interfaces/
│   │       └── IDatabaseService.cs
│   │
│   ├── OSHEngine.Data/                 # Database Operations & Scripts
│   │   ├── Scripts/
│   │   │   ├── 01_Schema.sql           # Database tables & logging schemas
│   │   │   └── 02_StoredProcedures.sql # usp_ReconcileInboundHealthData
│   │   └── DatabaseService.cs          # Direct ADO.NET or Dapper calls
│   │
│   └── OSHEngine.WorkerService/        # Background Host & File System Watchers
│       ├── Workers/
│       │   └── InboundDataWatcher.cs   # File monitoring logic
│       ├── Program.cs
│       └── appsettings.json            # SQL Connection strings
│
├── tests/
│   └── OSHEngine.Tests/                # Integration testing files
│       └── PipelineTests.cs
│
└── OSH-EHR-DataPipeline.sln
