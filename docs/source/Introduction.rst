.. _introduction:

How to Train a Language Model
=============================

Introduction
------------

This document explains how to train and package a language model for deployment.

You will usually want to deploy a language model in production. A good language model will improve transcription accuracy by correcting predictable spelling and grammatical mistakes. If you can predict what kind of speech your 🐸STT will encounter, you can make great gains in accuracy with a custom language model.

For example, if you want to transcribe university lectures on biology, you should train a language model on text related to biology. With this biology-specific language model, 🐸STT will be able to better recognize rare, hard to spell words like "cytokinesis".

How to train a model
--------------------

There are three steps to deploying a new language model for 🐸STT:

1. Identify and format text data for training
2. Train a `KenLM <https://github.com/kpu/kenlm>`_ language model using ``data/lm/generate_lm.py``
3. Package the model for deployment with ``generate_scorer_package``
