# XOps Microchallenge #8 – ConfigMaps vs Secrets ⚡

This challenge demonstrates how to use **Kubernetes ConfigMaps** for non-sensitive configuration and **Secrets** for sensitive data like credentials.

---

## ConfigMaps
- Store **non-sensitive configuration** such as environment settings, feature flags, or app properties.
- Example:  
  - `APP_MODE=dev`  
  - `FEATURE_X_ENABLED=true`
- Can be injected into pods as:
  - ✅ Environment variables  
  - ✅ Mounted files  

---

## Secrets
- Store **sensitive data** such as credentials, API tokens, certificates.
- Data is **base64-encoded** (not encrypted by default).
- Can be injected into pods as:
  - ✅ Environment variables  
  - ✅ Mounted files  
- Should be encrypted at rest using **KMS** for security.

---

## Best Practices
✅ Use **ConfigMaps** for non-sensitive app configs  
✅ Use **Secrets** for passwords, tokens, certificates  
✅ Never store sensitive data in ConfigMaps  
✅ Enable **encryption at rest** for Secrets  
✅ Use **RBAC** to restrict access to Secrets  

---

## Verification Screenshots

### 🔹 ConfigMap as environment variables ✅
<img width="1392" height="623" alt="Screenshot 2025-10-03 125042" src="https://github.com/user-attachments/assets/ed9f940d-e4b6-47dd-b752-14970971ed3c" />


---

### 🔹 ConfigMap mounted as files ✅
<img width="1376" height="140" alt="Screenshot 2025-10-03 125112" src="https://github.com/user-attachments/assets/0b8e9025-eb66-4dd7-84b0-518d13df23db" />


---

### 🔹 Secret injected as environment variables ✅
<img width="1386" height="262" alt="Screenshot 2025-10-03 125131" src="https://github.com/user-attachments/assets/4ef92f66-3d9b-4f5b-8ece-b7a3f7cd37f3" />


---

## ✅ Summary
- **ConfigMaps** → Non-sensitive configs (env vars, feature flags, app settings).  
- **Secrets** → Sensitive data (DB creds, API keys, certificates).  
- Together, they help keep configuration flexible and secure in Kubernetes.  
