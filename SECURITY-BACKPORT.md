# SigV4a security backport

Source: awslabs/aws-sdk-rust, SDK commit 3a3f39bd932690cab6d2321b677e97a24b687753, aws-sigv4 1.6.3 (Apache-2.0).

crypto-bigint を 0.7.6 へ更新し、RUSTSEC-2026-0387 に対応する。SDK の他クレートは公開版と同じ crates.io の依存を使い、型の重複を避ける。巨大な SDK 全体の取得を避けるため、このブランチには署名クレートだけを収録する。

検証: Rust 1.99.0、fmt、all-targets/all-features clippy (-D warnings)、署名テストベクトルを含む 133 tests passed / 10 ignored。
